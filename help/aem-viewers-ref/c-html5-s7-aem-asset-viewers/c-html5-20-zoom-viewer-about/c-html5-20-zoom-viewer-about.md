---
title: Zoom
description: Zoom Viewer é um visualizador de imagens que exibe uma imagem com zoom. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele tem ferramentas de zoom, suporte para tela cheia, amostras e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 0%

---

# Zoom{#zoom}

Zoom Viewer é um visualizador de imagens que exibe uma imagem com zoom. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele tem ferramentas de zoom, suporte para tela cheia, amostras e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador.

Visualizador tipo 502.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Usando o visualizador de zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de zoom representa um arquivo principal do JavaScript e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de zoom no modo pop-up usando uma página de HTML pronta para produção fornecida com Visualizadores IS ou no modo incorporado, onde ela é integrada à página da Web de destino usando a API documentada.

A configuração e a aparência são semelhantes às dos outros visualizadores. Toda a atribuição de capa é obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Zoom Viewer suporta os seguintes gestos de toque que são comuns em outros aplicativos móveis. Quando o visualizador não consegue processar o gesto de deslizar do usuário, ele encaminha o evento para o navegador da Web para executar a rolagem de página nativa. Esse tipo de funcionalidade permite que o usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área da tela do dispositivo.

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
   <td colname="col2"> <p> Seleciona a nova miniatura nas amostras. Na visualização principal, ela oculta ou revela elementos da interface do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque duas vezes </p> </td> 
   <td colname="col2"> <p> Amplia um nível até atingir a ampliação máxima. O próximo gesto de toque duplo redefine o visualizador para o estado de visualização inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apertar </p> </td> 
   <td colname="col2"> <p>Aumenta ou diminui o zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou mover horizontalmente </p> </td> 
   <td colname="col2"> <p> Rola pela lista de amostras na barra de amostras. </p> <p> Se a imagem estiver em um estado redefinido e o parâmetro </span> frametransition <span class="codeph"> estiver definido como slide, o ativo será alterado com a animação do slide. Para outros modos <span class="codeph"> frametransition </span>, o gesto executa a rolagem de página nativa. </p> <p> Se o zoom da imagem for ampliado, ela moverá a imagem horizontalmente. Se a imagem for movida para a borda da exibição e um deslizamento for executado na mesma direção, o gesto executará a rolagem de página nativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deslizamento vertical </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, o gesto executará a rolagem de página nativa. </p> <p> Quando o zoom da imagem é ampliado, ela move a imagem verticalmente. Se a imagem for movida para a borda de exibição e um deslizamento for executado na mesma direção, o gesto executará a rolagem de página nativa. </p> <p> Se o gesto for feito na área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador é compatível com entrada por toque e entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter layout estático ou usar design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador é compatível com três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento de HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página de HTML pronta para uso para o modo de operação pop-up. A página de HTML pronta para uso é chamada `ZoomViewer.html` e está localizada na subpasta `html5/` da sua implantação padrão de visualizadores IS, como no exemplo a seguir:

`<s7viewers_root>/html5/ZoomViewer.html`

Aplique CSS personalizado para obter uma aparência personalizada para a página.

Veja a seguir um exemplo do código HTML que abre o visualizador na nova janela:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do espaço imobiliário da página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas projetadas responsivas que ajustam o layout automaticamente, dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor opção para páginas da Web com layout estático.

O modo de incorporação de design responsivo presume que o redimensionamento do visualizador é necessário durante o tempo de execução devido à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir apenas a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa lógica garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas, como Bootstrap e Foundation.

Se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, ele preencherá essa área e seguirá o tamanho fornecido pela página da Web. Por exemplo, incorporar o visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

## Incorporação de tamanho fixo {#section-44f365e6c0dd40709467a459afa82a7f}

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua [!DNL ZoomViewer.js]. O arquivo [!DNL ZoomViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do SDK HTML5 carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, a inserção de uma referência direta a qualquer JavaScript `include` secundário usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do container DIV.

   Adicione um elemento DIV vazio à página em que você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definindo o tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens, em sistemas desktop, as miniaturas são colocadas abaixo da exibição principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal em tempo de execução usando a API `setAsset()`. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na parte inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e permitir que a exibição principal aumente sua altura e ocupe a área de miniaturas. Ou você pode manter o tamanho de exibição principal estático e recolher a área externa do visualizador, permitindo que o conteúdo da página da Web se mova para cima e usar o espaço livre restante na tela das miniaturas.

   Para manter intactos os limites do visualizador externo, defina o tamanho da classe CSS de nível superior `.s7zoomviewer` em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página do HTML. Ou ele pode ser colocado em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou transmitido explicitamente usando um comando de estilo.

   Consulte [Personalizando o visualizador de zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador externo estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com um visualizador externo fixo no exemplo a seguir. Observe que, ao alternar entre conjuntos, o tamanho do visualizador externo não é alterado:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=pt-BR](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=pt-BR)

   Para tornar as dimensões de exibição principais estáticas, defina o tamanho do visualizador em unidades absolutas para o componente SDK `Container` interno usando o seletor de CSS `.s7zoomviewer` `.s7container` ou usando o modificador `stagesize`.

   Este é um exemplo de definição do tamanho do visualizador para o componente SDK `Container` interno para que a área de exibição principal não altere seu tamanho ao alternar o ativo:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de demonstração a seguir mostra o comportamento do visualizador com um tamanho de exibição principal fixo. Observe que quando você alternar entre conjuntos, a exibição principal permanecerá estática e o conteúdo da página da Web se moverá verticalmente.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=pt-BR](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=pt-BR)

   É possível definir o modificador `stagesize` no registro de predefinição do visualizador no Dynamic Media Classic. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de Comandos desta Ajuda, como a seguir:

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.ZoomViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador.

   As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner do visualizador e o objeto JSON `params` aninhado com parâmetros de configuração aos quais o visualizador dá suporte. Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passagem das opções de configuração mínimas necessárias para o construtor e chamada do método `init()`. Este exemplo supõe que `zoomViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado DIV, `http://s7d1.scene7.com/is/image/` é a URL do Servidor de Imagens e `Scene7SharedAssets/ImageSet-Views-Sample` é o ativo.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de vídeo com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporação responsiva de design com altura irrestrita {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Com a incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para o exemplo a seguir, considere que a página da Web permite que o contêiner do visualizador `DIV` ocupe 40% do tamanho da janela do navegador da Web, deixando sua altura irrestrita. O código de HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que não é necessário definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicione o contêiner DIV ao `"holder"` DIV existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporação de tamanho flexível com largura e altura definidas {#section-3674e6c032594441a6576b7fb1de6e64}

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centralizá-lo na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` como 100%.

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Incorporação usando a API baseada em setter {#section-44e014925f24418b900696003855c0a9}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
