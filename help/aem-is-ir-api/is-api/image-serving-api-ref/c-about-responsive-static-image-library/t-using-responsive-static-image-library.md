---
description: Para adicionar a biblioteca de imagens responsivas a uma página da Web e gerenciar as imagens existentes com a biblioteca, conclua as seguintes etapas.
solution: Experience Manager
title: Uso da biblioteca de imagens responsivas
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---


# Usando a biblioteca de imagens responsivas{#using-responsive-image-library}

Para adicionar a biblioteca de imagens responsivas a uma página da Web e gerenciar as imagens existentes com a biblioteca, conclua as seguintes etapas.

**Para usar a biblioteca de imagens responsivas**

1. No Dynamic Media Classic, [crie uma predefinição de imagem](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) caso planeje usar a biblioteca de imagens responsivas com predefinições.

   Ao definir predefinições de imagens usadas com a Biblioteca de imagens responsivas, não use configurações que afetem o tamanho da imagem, como `wid=`, `hei=` ou `scl=`. Não especifique campos de tamanho na predefinição de imagem. Em vez disso, deixe-os como valores em branco.
1. Adicione o arquivo JavaScript da biblioteca à sua página da Web.

   Antes de usar a API de biblioteca, certifique-se de incluir `responsive_image.js`. Este arquivo JavaScript está localizado na subpasta `libs/` da sua implantação padrão do IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configure imagens existentes.

   A biblioteca lê determinados atributos de configuração de uma instância de imagem com a qual está trabalhando. Defina os atributos antes que a função da API `s7responsiveImage` seja chamada para essa imagem.

   Também é sugerido que você coloque o URL da imagem existente no atributo `data-src`. Em seguida, configure o atributo `src` existente para ter uma imagem GIF 1x1 codificada como URI de dados. Ao fazer isso, reduz o número de solicitações HTTP enviadas pela página da Web no tempo de carregamento. Observe, no entanto, que se SEO (otimização do mecanismo de pesquisa) for necessária, é melhor configurar um atributo `title` na instância da imagem.

   A seguir está um exemplo de definição do atributo `data-breakpoints` para a imagem e uso de um GIF 1x1 codificado como URI de dados:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Chame a função de API `s7responsiveImage` para cada instância de imagem gerenciada pela biblioteca.

   Chame a função de API `s7responsiveImage` para cada instância de imagem gerenciada pela biblioteca. Após essa chamada, a biblioteca substitui a imagem original pela imagem que é baixada do Serviço de imagem de acordo com o tamanho do tempo de execução do elemento `IMG` no layout da página da Web e a densidade da tela do dispositivo.

   O código a seguir é um exemplo de chamada da função `s7responsiveImage` API em uma imagem, considerando que `responsiveImage` é uma ID dessa imagem:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Exemplo {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

A biblioteca oferece suporte ao trabalho simultâneo com muitas instâncias de imagem na página da Web. Portanto, repita as etapas 1 e 2 acima para cada imagem que você deseja que a biblioteca gerencie.

É responsabilidade da página da Web estilizar o elemento de imagem para torná-lo flexível em tamanho. A própria biblioteca de imagens responsivas não diferencia entre imagens de tamanho fixo e &quot;fluidas&quot;. Se aplicada a uma imagem de tamanho fixo, ela carrega a nova imagem apenas uma vez.

O código a seguir é um exemplo completo de uma página trivial que tem uma única imagem fluida gerenciada pela biblioteca de imagens responsivas. O exemplo contém estilização de CSS extra para tornar a imagem &quot;responsiva&quot; ao tamanho da janela do navegador da Web:

```
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

**Uso de Recorte Inteligente**

Há dois modos de Recorte inteligente disponíveis no AEM 6.4 e no Dynamic Media Viewers 5.9:

* **Manual**  - os pontos de interrupção definidos pelo usuário e os comandos correspondentes do Serviço de imagem são definidos dentro de um atributo no elemento de imagem.
* **Recorte**  inteligente - execuções de recorte inteligente calculadas são recuperadas automaticamente do servidor de delivery. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo de Recorte inteligente, defina o atributo `data-mode` como `smart crop`. Por exemplo:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado despacha um evento `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção é alterado.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
