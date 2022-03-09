---
title: Uso da biblioteca de imagens responsivas
description: Para adicionar a biblioteca de Imagem responsiva a uma página da Web e gerenciar imagens existentes com a biblioteca, conclua as etapas a seguir.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Uso da biblioteca de imagens responsivas{#using-responsive-image-library}

Para adicionar a biblioteca de Imagem responsiva a uma página da Web e gerenciar imagens existentes com a biblioteca, conclua as etapas a seguir.

**Para usar a biblioteca de imagens responsivas**

1. No Dynamic Media Classic, [criar uma predefinição de imagem](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) caso planeje usar a biblioteca de Imagem responsiva com predefinições.

   Ao definir Predefinições de imagem usadas com a Biblioteca de imagens responsivas, não use configurações que afetem o tamanho da imagem, como `wid=`, `hei=`ou `scl=`. Não especifique nenhum campo de tamanho na Predefinição de imagem. Em vez disso, deixe-os como valores em branco.
1. Adicione o arquivo JavaScript da biblioteca à página da Web.

   Antes de usar a API da biblioteca, verifique se você inclui `responsive_image.js`. Esse arquivo JavaScript está localizado na variável `libs/` subpasta da sua implantação padrão do IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configure imagens existentes.

   A biblioteca lê determinados atributos de configuração de uma instância de imagem com a qual está trabalhando. Defina os atributos antes da `s7responsiveImage` A função da API é chamada para essa imagem.

   Também é sugerido colocar o URL da imagem existente no `data-src` atributo. Em seguida, configure a variável `src` para ter uma imagem GIF 1x1 codificada como URI de dados. Isso reduz o número de solicitações HTTP enviadas pela página da Web no momento do carregamento. Observe, no entanto, que se SEO (otimização de mecanismo de pesquisa) for necessário, é melhor configurar um `title` na instância da imagem.

   Este é um exemplo de definição `data-breakpoints` para a imagem e usando um GIF 1x1 codificado como URI de dados:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Chame o `s7responsiveImage` Função de API para cada instância de imagem que a biblioteca gerencia.

   Chame o `s7responsiveImage` Função de API para cada instância de imagem que a biblioteca gerencia. Após essa chamada, a biblioteca substitui a imagem original pela imagem que é baixada do Serviço de imagem de acordo com o tamanho de tempo de execução da variável `IMG` no layout da página da Web e na densidade da tela do dispositivo.

   O código a seguir é um exemplo de chamada de `s7responsiveImage` Função da API em uma imagem, supondo que `responsiveImage` é uma ID dessa imagem:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemplo {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

A biblioteca suporta o trabalho simultâneo com muitas instâncias de imagem na página da Web. Portanto, repita as etapas 1 e 2 acima para cada imagem que você deseja que a biblioteca gerencie.

É de responsabilidade da página da Web estilizar o elemento de imagem para torná-lo flexível em tamanho. A própria biblioteca de Imagem responsiva não diferencia entre imagens de tamanho fixo e &quot;fluidas&quot;. Se aplicada a uma imagem de tamanho fixo, ela carregará a nova imagem apenas uma vez.

O código a seguir é um exemplo completo de uma página da Web trivial que tem uma única imagem fluida gerenciada pela biblioteca de Imagem Responsiva. O exemplo contém um estilo de CSS extra para tornar a imagem &quot;responsiva&quot; ao tamanho da janela do navegador da Web:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Uso do Recorte Inteligente**

Há dois modos de Recorte inteligente disponíveis no AEM 6.4 e no Dynamic Media Viewers 5.9:

* **Manual** - os pontos de interrupção definidos pelo usuário e os comandos correspondentes do Serviço de imagem são definidos dentro de um atributo no elemento de imagem.
* **Corte inteligente** - as representações de recorte inteligente calculadas são recuperadas automaticamente do servidor de delivery. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo Corte inteligente, defina o `data-mode` para `smart crop`. Por exemplo:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado envia um `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção for alterado.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
