---
title: Uso da biblioteca de imagens responsiva
description: Para adicionar a Biblioteca de imagens responsiva a uma página da Web e gerenciar imagens existentes com a biblioteca, conclua as etapas a seguir.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Uso da biblioteca de imagens responsiva{#using-responsive-image-library}

Para adicionar a Biblioteca de imagens responsiva a uma página da Web e gerenciar imagens existentes com a biblioteca, conclua as etapas a seguir.

**Para usar a Biblioteca de imagens responsiva**

1. No Dynamic Media Classic, [crie uma Predefinição de imagem](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=pt-BR#image-sizing) caso planeje usar a biblioteca de Imagens responsivas com predefinições.

   Ao definir as Predefinições de imagem usadas com a Biblioteca de imagens responsiva, não use configurações que afetem o tamanho da imagem, como `wid=`, `hei=` ou `scl=`. Não especifique campos de tamanho na Predefinição de imagem. Em vez disso, deixe-os como valores em branco.
1. Adicione o arquivo JavaScript da biblioteca à página da Web.

   Antes de poder usar a API da biblioteca, certifique-se de incluir `responsive_image.js`. Esse arquivo do JavaScript está localizado na subpasta `libs/` da sua implantação padrão do IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurar imagens existentes.

   A biblioteca lê determinados atributos de configuração de uma instância de imagem com a qual está trabalhando. Defina os atributos antes que a função da API `s7responsiveImage` seja chamada para essa imagem.

   Também é recomendável colocar a URL da imagem existente no atributo `data-src`. Em seguida, configure o atributo `src` existente para ter uma imagem GIF 1x1 codificada como URI de Dados. Ao fazer isso, o reduz o número de solicitações HTTP enviadas pela página da Web no momento do carregamento. Observe, no entanto, que se a SEO (otimização do mecanismo de pesquisa) for necessária, é melhor configurar um atributo `title` na instância da imagem.

<!--
   The following is an example of defining `data-breakpoints` attribute for the image and using a 1x1 GIF encoded as Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```
-->

1. Chame a função de API `s7responsiveImage` para cada instância de imagem gerenciada pela biblioteca.

   Chame a função de API `s7responsiveImage` para cada instância de imagem gerenciada pela biblioteca. Após essa chamada, a biblioteca substituirá a imagem original pela imagem baixada do Servidor de imagens, de acordo com o tamanho do tempo de execução do elemento `IMG` no layout da página da Web e a densidade da tela do dispositivo.

   O código a seguir é um exemplo de chamada à função de API `s7responsiveImage` em uma imagem, supondo que `responsiveImage` seja uma ID dessa imagem:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemplo {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

A biblioteca é compatível com o trabalho simultâneo com muitas instâncias de imagem na página da Web. Portanto, repita as etapas 1 e 2 acima para cada imagem que você deseja que a biblioteca gerencie.

É responsabilidade da página da Web estilizar o elemento de imagem para torná-lo flexível em tamanho. A própria biblioteca de imagens responsivas não diferencia imagens de tamanho fixo de imagens &quot;fluídas&quot;. Se aplicada a uma imagem de tamanho fixo, ela carrega a nova imagem apenas uma vez.

<!--
The following code is a complete example of a trivial web page that has a single fluid image managed by the Responsive Image library. The example contains extra CSS styling to make the image "responsive" to the web browser window size:

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
-->

**Usando o Corte Inteligente**

Há dois modos de Corte inteligente disponíveis no AEM 6.4 e nos Visualizadores do Dynamic Media 5.9:

* **Manual** - os pontos de interrupção definidos pelo usuário e os comandos de Serviço de Imagem correspondentes são definidos em um atributo no elemento de imagem.
* **Recorte inteligente** - as representações de recorte inteligente computadas são recuperadas automaticamente do servidor de entrega. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo Corte inteligente, você define o atributo `data-mode` como `smart crop`. Por exemplo:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado despacha um evento `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção é alterado.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
