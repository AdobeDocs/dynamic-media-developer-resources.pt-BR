---
title: Mix de mídia
description: O Visualizador de mídia mista é um visualizador de mídia. Ele é compatível com conjuntos de mídia que contêm imagens, conjuntos de amostras, conjuntos de rotação, vídeos e Conjuntos de vídeos adaptados.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2642'
ht-degree: 0%

---

# Mix de mídia{#mixed-media}

O Visualizador de mídia mista é um visualizador de mídia. Ele é compatível com conjuntos de mídia que contêm imagens, conjuntos de amostras, conjuntos de rotação, vídeos e Conjuntos de vídeos adaptados.

Uma miniatura na parte inferior do visualizador representa cada elemento de conjunto de mídia, juntamente com seu indicador de tipo de ativo. Quando um elemento do conjunto de amostras é selecionado, uma linha secundária de amostras é exibida para permitir a seleção da variação de cor no conjunto de amostras. Imagens e elementos de conjunto de amostras oferecem suporte ao zoom no modo contínuo ou em linha; os conjuntos de rotação oferecem suporte ao zoom e à rotação. Os vídeos e os Conjuntos de vídeos adaptados são compatíveis com todos os controles básicos de reprodução, desde que as legendas ocultas opcionais sejam exibidas sobre o conteúdo do vídeo. Um usuário pode alternar para o modo de tela cheia a qualquer momento clicando no botão de tela cheia. O visualizador tem o botão Fechar opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.

O Visualizador de mídia mista usa a reprodução de vídeo de transmissão HTML5 no formato HLS na configuração padrão, sempre que o sistema subjacente oferece suporte a isso. Em sistemas que não suportam transmissão contínua de HTML5, o visualizador retorna à entrega de vídeo progressiva de HTML5.

>[!NOTE]
>
>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador.

Visualizador tipo 505.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Uso do visualizador de mix de mídia {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de mídia mista representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de mídia mista no modo pop-up usando a página de HTML pronta para produção fornecida com os Visualizadores IS. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado em uma página da Web de destino usando a API documentada.

A tarefa de configurar e definir a aparência do visualizador é semelhante a outros visualizadores. Toda a atribuição de capa é obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de mix de mídia {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de mídia mista é compatível com gestos de toque único e multitoque comuns em outros aplicativos móveis. Quando o visualizador não consegue processar o gesto de deslizar de um usuário, ele encaminha o evento para o navegador da Web para executar uma rolagem de página nativa. Essa funcionalidade permite que um usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área da tela do dispositivo.

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
   <td colname="col2"> <p> Ativa a exibição de imagem suspensa ou altera entre os níveis de zoom primário e secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque duas vezes </p> </td> 
   <td colname="col2"> <p>Quando em <span class="codeph"> contínuo </span> modo de zoom, aumenta o zoom em um nível até que a ampliação máxima seja atingida, o próximo gesto de toque duplo é redefinido para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque e segure </p> </td> 
   <td colname="col2"> <p> Quando em <span class="codeph"> em linha </span> modo de zoom, ativa a imagem com zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apertar </p> </td> 
   <td colname="col2"> <p>No modo de zoom contínuo, aumenta ou diminui o zoom da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou mover horizontalmente </p> </td> 
   <td colname="col2"> <p> Quando o ativo atual é um conjunto de rotação e a imagem está em um estado de redefinição, ela gira horizontalmente pelo conjunto de rotação. </p> <p> Quando o ativo atual é um conjunto de rotação ou uma imagem e o zoom da imagem é aplicado, ele move a imagem horizontalmente. Se a imagem for movida para a borda da exibição e o deslizamento ainda for feito nessa direção, o gesto executará uma rolagem de página nativa. </p> <p> Rola pela lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar o dedo ou mover-se verticalmente </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, ela alterará o ângulo de exibição vertical caso um conjunto de rotação multidimensional seja usado. Em um conjunto de rotação unidimensional, ou quando um conjunto de rotação multidimensional está no último ou no primeiro eixo, de modo que o deslizamento vertical não resulte na alteração do ângulo de exibição vertical, o gesto executa a rolagem de página nativa. </p> <p> Quando o ativo atual é um conjunto de rotação ou uma imagem e a imagem é ampliada, move a imagem verticalmente. Se a imagem for movida para a borda da exibição e o deslizamento ainda for feito nessa direção, o gesto executará a rolagem de página nativa. </p> <p> Se o gesto for feito na área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada por toque e à entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação pelo teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de mix de mídia {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador é compatível com três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

## Sobre o modo pop-up {#section-77d5aa03b8b94566958a179b1a2cd474}

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ele ocupa toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação de um dispositivo móvel seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` Chamada de JavaScript, configurada corretamente `A` elemento HTML ou qualquer outro método adequado.

É recomendável usar uma página de HTML pronta para uso para o modo de operação pop-up. Nesse caso, é chamado de [!DNL MixedMediaViewer.html] e estiver localizado na [!DNL html5/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Veja a seguir um exemplo do código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Sobre tamanho fixo e incorporação responsiva de design {#section-ec86b100ba5943d0b16694268520bbde}

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio imobiliário de uma página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablet e também páginas de design responsivas que ajustam o layout automaticamente, dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa ação é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva de design presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura irrestrita, o visualizador escolhe automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap ou Foundation.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preenche apenas essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

## Incorporação de tamanho fixo {#section-17d162f76ffa4804b27928f51e7bea1d}

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do contêiner `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua [!DNL MixedMediaViewer.js]. A variável [!DNL MixedMediaViewer.js] O arquivo está localizado sob o [!DNL html5/js/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Fazer referência apenas ao JavaScript do visualizador principal `include` arquivo na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Em particular, não faça referência direta ao SDK do HTML5 `Utils.js` biblioteca carregada pelo visualizador de `/s7viewers` caminho de contexto (o chamado SDK consolidado) `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução são totalmente gerenciadas pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, ao inserir uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do container DIV.

   Adicione um elemento DIV vazio à página em que você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio de CSS.

   O espaço reservado DIV é um elemento posicionado, o que significa que o `position` A propriedade CSS está definida como `relative` ou `absolute`.

   Verifique se o recurso de tela cheia funciona corretamente no Internet Explorer. Verifique se não há outros elementos no DOM com uma ordem de empilhamento superior à do espaço reservado DIV.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Definir o tamanho do visualizador

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Nos sistemas desktop, as miniaturas são colocadas abaixo da exibição principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando `setAsset()` API. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na parte inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e permitir que a exibição principal aumente sua altura e ocupe a área de miniaturas. Ou você pode manter o tamanho da exibição principal estático e recolher a área externa do visualizador, permitindo que o conteúdo da página da Web se mova para cima. Em seguida, use o espaço livre deixado pelas miniaturas.

   Para manter intactos os limites do visualizador externo, defina o tamanho para `.s7mixedmediaviewer` classe CSS de nível superior em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado e, posteriormente, atribuído a um registro predefinido do visualizador no Dynamic Media Classic, ou passado explicitamente usando o comando style.

   Consulte [Personalização do visualizador de mix de mídia](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) para obter mais informações sobre como estilizar o visualizador com CSS.

   Veja a seguir um exemplo de definição do tamanho estático do visualizador externo em uma página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na página de exemplo a seguir. Observe que, ao alternar entre conjuntos, o tamanho do visualizador externo não é alterado:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Para tornar as dimensões de exibição principais estáticas, defina o tamanho do visualizador em unidades absolutas para o painel interno `Container` Componente do SDK usando `.s7mixedmediaviewer .s7container` Seletor de CSS ou usando `stagesize` modificador.

   Veja a seguir um exemplo de definição do tamanho do visualizador para o `Container` Componente do SDK para que a área de exibição principal não altere o tamanho ao alternar o ativo:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de exemplo a seguir mostra o comportamento do visualizador com um tamanho de exibição principal fixo. Observe que quando você alternar entre conjuntos, a exibição principal permanecerá estática e o conteúdo da página da Web se moverá verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   Você pode definir a variável `stagesize` modificador no registro predefinido do visualizador no Dynamic Media Classic, ou passe-o explicitamente com o código de inicialização do visualizador com `params` coleção. Ou, como uma chamada de API, conforme descrito na seção Referência de comandos desta Ajuda, como no exemplo a seguir:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância de `s7viewers.MixedMediaViewer` classe, transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter a `containerId` campo que contém o nome da ID do contêiner de visualização e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador. Neste caso, o `params` objeto deve ter pelo menos o URL do Servidor de imagens passado como `serverUrl` propriedade, o URL do servidor de vídeo passado como `videoserverurl` propriedade e ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o `init()` método antes do fechamento `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, pode ser oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmissão das opções de configuração mínimas necessárias para o construtor e chamada de `init()` método. O exemplo assume `mixedMediaViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; [!DNL http://s7d1.scene7.com/is/image/] é o URL do Servidor de Imagens; [!DNL http://s7d1.scene7.com/is/content/] é o URL do servidor de vídeo; e [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] é o ativo:

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de mídia mista com um tamanho fixo:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporação responsiva com altura irrestrita {#section-056cb574713c4d07be6d07cf3c598839}

Com a incorporação responsiva de design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do container do visualizador `DIV`. Para o exemplo a seguir, considere que a página da Web permite o container do visualizador `DIV` para obter 40% do tamanho da janela do navegador web, deixando sua altura irrestrita. O código de HTML da página da Web seria semelhante ao seguinte:

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

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicionar o contêiner DIV ao existente `"holder"` DIV O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incorporação de tamanho flexível com largura e altura definidas {#section-0a329016f9414d199039776645c693de}

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centraliza na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%.

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporação usando a API baseada em setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`, e `setAsset()` Métodos de API do, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
