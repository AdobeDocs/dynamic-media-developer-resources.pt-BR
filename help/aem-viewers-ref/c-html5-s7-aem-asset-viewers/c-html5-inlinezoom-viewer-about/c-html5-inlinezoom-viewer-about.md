---
title: Zoom in-line
description: O Visualizador de zoom incorporado é um visualizador de imagens. Ele exibe uma imagem estática com a versão com zoom mostrada sobre a imagem estática quando um usuário passa sobre ou toca a visualização principal. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# Zoom in-line{#inline-zoom}

O Visualizador de zoom incorporado é um visualizador de imagens. Ele exibe uma imagem estática com a versão com zoom mostrada sobre a imagem estática quando um usuário passa sobre ou toca a visualização principal. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador.

Tipo de visualizador 504.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400)

## Usando o Visualizador de zoom incorporado {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de zoom integrado representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do Visualizador SDK usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador no tempo de execução.

O Visualizador de zoom em linha pode ser usado no modo pop-up usando a página do HTML pronta para produção fornecida com os Visualizadores do servidor de imagens ou no modo incorporado, onde é integrado em uma página da Web de destino usando a API documentada.

A configuração e a aparência são semelhantes às dos outros visualizadores. Você pode usar CSS personalizado para aplicar a atribuição de capa.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o visualizador de zoom em linha {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de zoom integrado suporta gestos de toque único e multitoque comuns em outros aplicativos móveis.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Toque único </p> </td> 
   <td colname="col2"> <p> Ativa a exibição de imagem suspensa ou altera entre o nível de zoom primário e secundário nas amostras, seleciona uma nova miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou mover horizontalmente </p> </td> 
   <td colname="col2"> <p> Rola pela lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deslizamento vertical </p> </td> 
   <td colname="col2"> <p>Se o gesto for feito na área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada por toque e à entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de zoom em linha {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link clicável que abre o visualizador em uma janela do navegador separada. Em outros casos, pode ser necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador é compatível com três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva.

**Pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e se ajusta quando a janela do navegador é redimensionada ou a orientação do dispositivo é alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento do HTML `A` configurado corretamente ou qualquer outra maneira adequada.

É recomendável usar a página predefinida do HTML para o modo pop-up chamado `FlyoutViewer.html`. Está localizado na subpasta [!DNL html5/] da sua implantação padrão do Image Serving-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

Também é necessário ter o componente FlyoutZoomView configurado para funcionar no modo de zoom em linha. É recomendável usar a predefinição `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` pronta para uso do visualizador de Zoom incorporado ou uma predefinição personalizada derivada dela. A personalização visual pode ser obtida ao aplicar CSS personalizado.

Veja a seguir um exemplo de código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Inserção de Tamanho Fixo e Inserção Responsiva**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do espaço físico da página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas da Web responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

O modo de incorporação de tamanho fixo é usado quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é melhor para páginas da Web com layout de página estático.

O modo de incorporação de design responsivo presume que o visualizador deve redimensionar durante o tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

Ao usar o modo de incorporação de design responsivo com o Visualizador de zoom em linha, especifique pontos de interrupção explícitos para a imagem de exibição principal usando o parâmetro `imagereload`. Idealmente, associe seus pontos de interrupção com os pontos de interrupção de largura do visualizador, conforme ditado pelo CSS da página da Web.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da maneira como um contêiner de página da Web `DIV` é dimensionado. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade significa que o ativo se encaixa perfeitamente na exibição sem qualquer preenchimento nas laterais. Esse caso de uso específico é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap ou Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá somente essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo de caso de uso é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho do HTML. Antes de usar a API do visualizador, inclua `FlyoutViewer.js`. `FlyoutViewer.js` está na seguinte subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media que têm os Visualizadores IS instalados.

Um caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do HTML5 SDK carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, a inserção de uma referência direta a qualquer JavaScript `include` secundário usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do container DIV.

   Adicione um elemento DIV vazio à página em que você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   É de responsabilidade da página da Web especificar o `z-index` correto para o elemento DIV de espaço reservado. Isso garante que a parte da imagem suspensa do visualizador apareça sobre os outros elementos da página da Web.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Definindo o tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Nos sistemas desktop, as miniaturas são colocadas abaixo da exibição principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando a API `setAsset()`. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na área inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e permitir que a exibição principal aumente sua altura e ocupe a área de miniaturas. Ou você pode manter o tamanho de exibição principal estático e recolher a área do visualizador externo, permitindo que o conteúdo da página da Web se mova para cima e usar o espaço livre da página deixado nas miniaturas.

   Para manter intactos os limites do visualizador externo, defina o tamanho para a classe CSS de nível superior `.s7flyoutviewer` em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado e, posteriormente, atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou passado explicitamente usando o comando style.

   Consulte [Personalizando o visualizador de zoom embutido](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição do tamanho estático do visualizador externo em uma página do HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na página de exemplo a seguir. Observe que, ao alternar entre conjuntos, o tamanho do visualizador externo não é alterado:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   Para tornar as dimensões de exibição principais estáticas, defina o tamanho do visualizador em unidades absolutas para o componente SDK `Container` interno usando o seletor CSS `.s7flyoutviewer .s7container`. Além disso, você deve substituir o tamanho fixo definido para a classe CSS de nível superior `.s7flyoutviewer` no CSS do visualizador padrão, definindo-o como `auto`.

   Este é um exemplo de definição do tamanho do visualizador para o componente interno do SDK `Container` para que a área de exibição principal não altere seu tamanho ao alternar o ativo:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de exemplo a seguir mostra o comportamento do visualizador com um tamanho de exibição principal fixo. Observe que quando você alternar entre conjuntos, a exibição principal permanecerá estática e o conteúdo da página da Web se moverá verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   Além disso, o CSS do visualizador padrão fornece um tamanho fixo para sua área externa pronta para uso.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.FlyoutViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner de visualizador e o objeto JSON `params` aninhado com parâmetros de configuração aos quais o visualizador dá suporte. Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de Imagens passada como propriedade `serverUrl`; o ativo inicial como parâmetro `asset`, caminho base para carregar CSS como parâmetro `contentUrl` e nome predefinido como parâmetro `config`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação acontece, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando as opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. O exemplo considera `inlineZoomViewer` como a instância do visualizador; `s7viewer` como o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` como a URL do Servidor de Imagens; e `Scene7SharedAssets/ImageSet-Views-Sample` como o ativo:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de zoom em linha com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporação responsiva de design com altura irrestrita {#section-056cb574713c4d07be6d07cf3c598839}

Com a incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para o exemplo a seguir, considere que a página da Web permite que o contêiner do visualizador `DIV` ocupe 40% do tamanho da janela do navegador da Web, deixando sua altura irrestrita. O código HTML da página da Web seria semelhante ao seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você deve substituir o tamanho fixo do CSS do visualizador padrão pelo tamanho definido em unidades relativas.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo, com as três exceções a seguir:

* adicionar o contêiner `DIV` ao &quot;proprietário&quot; existente `DIV`;
* adicionado o parâmetro `imagereload` com pontos de interrupção explícitos;
* em vez de definir um tamanho de visualizador fixo usando unidades absolutas, use CSS que defina o visualizador `width` e `height` como 100% como no seguinte:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações em tempo real](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incorporação de tamanho flexível com largura e altura definidas {#section-0a329016f9414d199039776645c693de}

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` como 100%.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

O restante das etapas de incorporação são idênticas às etapas usadas para incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporação usando a API baseada em setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()`, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
