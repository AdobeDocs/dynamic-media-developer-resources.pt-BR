---
title: Tutorial do visualizador do SDK
description: O SDK do visualizador fornece um conjunto de componentes baseados em JavaScript para o desenvolvimento de visualizadores personalizados. Os visualizadores são aplicativos baseados na Web que permitem que o conteúdo de mídia avançada veiculado pelo Adobe Dynamic Media seja incorporado a páginas da Web.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Tutorial do visualizador do SDK{#viewer-sdk-tutorial}

O SDK do visualizador fornece um conjunto de componentes baseados em JavaScript para o desenvolvimento de visualizadores personalizados. Os visualizadores são aplicativos baseados na Web que permitem que o conteúdo de mídia avançada veiculado pelo Adobe Dynamic Media seja incorporado a páginas da Web.

Por exemplo, o SDK fornece zoom e panorama interativos. Ele também fornece visualização e reprodução de vídeo de 360° dos ativos que foram carregados para o Adobe Dynamic Media por meio do aplicativo de back-end chamado Dynamic Media Classic.

Embora os componentes dependam da funcionalidade do HTML5, eles foram projetados para funcionar em dispositivos e desktops Android™ e Apple iOS, incluindo o Internet Explorer e versões posteriores. Esse tipo de experiência significa que você pode fornecer um único fluxo de trabalho para todas as plataformas compatíveis.

O SDK consiste em componentes de interface do usuário que compõem o conteúdo do visualizador. É possível estilizar esses componentes por meio de CSS e componentes que não sejam de interface do usuário que tenham algum tipo de função de suporte, como busca e análise de definição de conjunto ou rastreamento. Todos os comportamentos de componentes são personalizáveis por meio de modificadores que podem ser especificados de várias maneiras, por exemplo, como `name=value` pares no URL.

Este tutorial inclui a seguinte ordem de tarefas para ajudar você a criar um visualizador de zoom básico:

* [Baixe o SDK do visualizador mais recente da Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Carregar o SDK do visualizador](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Adicionar estilo ao visualizador](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Incluindo Container e ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Adição dos componentes MediaSet e Amostras ao visualizador](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Adição de botões ao visualizador](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configuração das amostras verticalmente](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Baixe o SDK do visualizador mais recente da Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Baixe o SDK do visualizador mais recente da Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >Você pode concluir este tutorial sem a necessidade de baixar o pacote do Visualizador SDK, pois o SDK é carregado remotamente. No entanto, o pacote do Visualizador inclui exemplos adicionais e um guia de referência de API que pode ajudar você a criar seus próprios visualizadores.

## Carregar o SDK do visualizador {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Comece configurando uma nova página para desenvolver o visualizador básico de zoom que você vai criar.

   Considere essa página atualizada como o código do Bootstrap ou carregador usado para configurar um aplicativo SDK vazio. Abra seu editor de texto favorito e cole a seguinte marcação HTML nele:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Adicione o seguinte código JavaScript dentro do `script` para inicializar o `ParameterManager`. Isso o ajuda a se preparar para criar e instanciar componentes do SDK dentro da `initViewer` função:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Salve o arquivo como um modelo vazio. Você pode usar qualquer nome de arquivo desejado.

   Você pode usar esse arquivo de modelo vazio como uma referência ao criar visualizadores no futuro. Esse template funciona localmente e quando veiculado a partir de um servidor Web.

Agora adicione o estilo ao visualizador.

## Adicionar estilo ao visualizador {#section-3783125360a1425eae5a5a334867cc32}

1. Para esse visualizador de página completo que você está criando, é possível adicionar alguns estilos básicos.

   Adicione o seguinte `style` bloco na parte inferior da `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Agora inclua os componentes `Container` e `ZoomView`.

## Incluindo Container e ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Criar um visualizador real incluindo os componentes `Container` e `ZoomView`.

   Insira o seguinte `include` instruções na parte inferior do `<head>` elemento — após a variável [!DNL Utils.js] o script é carregado:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Agora crie variáveis para fazer referência aos vários componentes do SDK.

   Adicione as seguintes variáveis na parte superior da função anônima principal, logo acima `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Insira o seguinte no `initViewer` para que você possa definir alguns modificadores e instanciar os respectivos componentes:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full-screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full-screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Para que o código acima seja executado corretamente, adicione uma `containerResize` manipulador de eventos e uma função auxiliar:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Visualize a página para que você possa ver o que criou. Sua página deve ser semelhante ao seguinte:

   ![Exemplo de visualizador em uma imagem](assets/viewer-1.jpg)

Agora adicione os componentes `MediaSet` e `Swatches` ao visualizador.

## Adição dos componentes MediaSet e Amostras ao visualizador {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Para conceder aos usuários a capacidade de selecionar imagens de um conjunto, é possível adicionar os componentes `MediaSet` e `Swatches`.

   Adicione os seguintes inclusões de SDK:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Atualize a lista de variáveis com o seguinte:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Instancie `MediaSet` e `Swatches` componentes dentro da `initViewer` função.

   Certifique-se de instanciar a variável `Swatches` instância após o `ZoomView` e `Container` componentes, caso contrário, a ordem de empilhamento ocultará a `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Agora adicione as seguintes funções de manipulador de eventos:

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Posicione as amostras na parte inferior do visualizador adicionando o seguinte CSS à `style` elemento:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Visualize seu visualizador.

   Observe que as amostras estão no canto inferior esquerdo do visualizador. Para que as amostras tenham toda a largura do visualizador, adicione uma chamada para redimensionar manualmente as amostras sempre que o usuário redimensionar o navegador. Adicione o seguinte à `resizeViewer` função:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   Agora o visualizador se parece com a imagem a seguir. Tente redimensionar a janela do navegador do visualizador e observe o comportamento resultante.

   ![Exemplo de duas imagens do visualizador](assets/viewer-2.jpg)

Agora, adicione os botões de ampliar, reduzir e redefinir o zoom ao visualizador.

## Adição de botões ao visualizador {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Atualmente, o usuário só pode aplicar zoom usando gestos de clique ou toque. Portanto, adicione alguns botões básicos de controle de zoom ao visualizador.

   Adicione os seguintes componentes de botão:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Atualize a lista de variáveis com o seguinte:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Botões Instanciar na parte inferior de `initViewer` função.

   Lembre-se de que a ordem é importante, a menos que você especifique a `z-index` no CSS:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Agora, defina alguns estilos básicos para os botões adicionando o seguinte à `style` bloco na parte superior do arquivo:

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Visualize seu visualizador. Ela deve ser semelhante ao seguinte:

   ![Exemplo de três imagens do visualizador](assets/viewer-3.jpg)

   Agora, configure as Amostras para que elas sejam alinhadas verticalmente à direita.

## Configuração das amostras verticalmente {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. É possível configurar modificadores diretamente no `ParameterManager` instância.

   Adicione o seguinte à parte superior da `initViewer` para que você possa configurar a função `Swatches` layout de miniatura como uma única linha:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Atualize a seguinte chamada de redimensionamento no `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Editar o seguinte `s7swatches` regra no `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Visualize seu visualizador. Ele tem a seguinte aparência:

   ![Exemplo de quatro imagens do visualizador](assets/viewer-4.jpg)

   O visualizador básico de zoom está concluído.

   Este tutorial do visualizador aborda os fundamentos do que o SDK do visualizador do Dynamic Media oferece. Ao trabalhar com o SDK, você pode usar os vários componentes padrão para criar e estilizar facilmente experiências de visualização avançadas para os públicos-alvo.
