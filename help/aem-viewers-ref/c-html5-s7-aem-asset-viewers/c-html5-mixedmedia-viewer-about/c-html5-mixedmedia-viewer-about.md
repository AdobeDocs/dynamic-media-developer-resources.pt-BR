---
description: O Mixed Media Viewer é um visualizador de mídia. Suporta conjuntos de mídia que contêm imagens, conjuntos de amostras, conjuntos de rotação, vídeos e Conjuntos de vídeo adaptáveis.
keywords: responsive
solution: Experience Manager
title: Mídia mista
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '2660'
ht-degree: 0%

---


# Mídia mista{#mixed-media}

O Mixed Media Viewer é um visualizador de mídia. Suporta conjuntos de mídia que contêm imagens, conjuntos de amostras, conjuntos de rotação, vídeos e Conjuntos de vídeo adaptáveis.

Uma miniatura na parte inferior do visualizador representa cada elemento de conjunto de mídia, juntamente com seu indicador de tipo de ativo. Quando um elemento de conjunto de amostras é selecionado, uma linha secundária de amostras é exibida para permitir a seleção da variação de cor dentro do conjunto de amostras. As imagens e os elementos do conjunto de amostras suportam o zoom no modo contínuo ou em linha; os conjuntos de rotação suportam zoom e rotação. Os vídeos e os Conjuntos de vídeos adaptativos suportam todos os controles básicos de reprodução, desde que as legendas ocultas opcionais sejam exibidas na parte superior do conteúdo do vídeo. Um usuário pode alternar para tela cheia a qualquer momento clicando no botão de tela cheia. O visualizador tem o botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.

O visualizador de mídia mista usa a reprodução de vídeo de streaming HTML5 no formato HLS em sua configuração padrão sempre que o sistema subjacente suportar isso. Em sistemas que não suportam streaming HTML5, o visualizador volta ao delivery de vídeo progressivo HTML5.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador.

Tipo de visualizador 505.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Usando o visualizador de mídia mista {#section-f21ac23d3f6449ad9765588d69584772}

O visualizador de mídia mista representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de mídia mista no modo pop-up usando a página HTML pronta para produção fornecida com os IS-Viewers. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado a uma página da Web do público alvo usando a API documentada.

A tarefa de configurar e captar o visualizador é semelhante a outros visualizadores. Todas as películas são obtidas por meio de CSS personalizado.

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de mídia mista {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O visualizador de mídia mista é compatível com gestos de toque único e multitoque comuns em outros aplicativos móveis. Quando o visualizador não puder processar o gesto de deslizamento de um usuário, ele encaminhará o evento para o navegador da Web para executar uma rolagem de página nativa. Essa funcionalidade permite que um usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área de tela do dispositivo.

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
   <td colname="col2"> <p> Ativa a visualização de flyout ou as alterações entre o nível de zoom primário e secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duplo </p> </td> 
   <td colname="col2"> <p>Quando em <span class="codeph"> modo de zoom contínuo </span>, o zoom é ampliado em um nível até que a ampliação máxima seja atingida, o gesto de toque do próximo duplo é redefinido para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque e segure </p> </td> 
   <td colname="col2"> <p> Quando em <span class="codeph"> modo de zoom incorporado </span>, ativa a imagem ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Quando no modo de zoom contínuo, a imagem é ampliada para dentro ou para fora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque horizontal ou toque </p> </td> 
   <td colname="col2"> <p> Quando o ativo atual é um conjunto de rotação e a imagem está em um estado de redefinição, ele gira pelo conjunto de rotação horizontalmente. </p> <p> Quando o ativo atual é um conjunto de rotação ou uma imagem e a imagem é ampliada, ela move a imagem horizontalmente. Se a imagem for movida para a borda da visualização e o deslizamento ainda for feito nessa direção, o gesto executará uma rolagem de página nativa. </p> <p> Percorre a lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque vertical ou clique </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, ela alterará o ângulo de visualização vertical caso um conjunto de rotação multidimensional seja usado. Em um conjunto de rotação unidimensional, ou quando um conjunto de rotação multidimensional está no último ou no primeiro eixo, de modo que o deslize vertical não resulta em alteração do ângulo de visualização vertical, o gesto executa a rolagem da página nativa. </p> <p> Quando o ativo atual é um conjunto de rotação ou uma imagem e a imagem é ampliada, move a imagem na vertical. Se a imagem for movida para a borda da visualização e o deslizamento ainda for feito nessa direção, o gesto executará a rolagem da página nativa. </p> <p> Se o gesto for feito dentro da área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada de toque e à entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Este visualizador está totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Como incorporar o Visualizador de Mídia Misto {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsivo.

## Sobre o modo pop-up {#section-77d5aa03b8b94566958a179b1a2cd474}

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação de um dispositivo móvel seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` chamada JavaScript, elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML predefinida para o modo de operação de pop-up. Nesse caso, ele é chamado [!DNL MixedMediaViewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

A seguir está um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Sobre a incorporação de tamanho fixo e design responsivo {#section-ec86b100ba5943d0b16694268520bbde}

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio de uma página da web.

Os casos de uso principal são páginas da Web orientadas para desktops ou tablets e também páginas de design responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web que têm um layout estático.

A incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à visualização, sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho que o layout da página da Web fornece. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

## Incorporação de tamanho fixo {#section-17d162f76ffa4804b27928f51e7bea1d}

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir [!DNL MixedMediaViewer.js]. O arquivo [!DNL MixedMediaViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal `include` na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca HTML5 SDK `Utils.js` carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o DIV do container.

   Adicione um elemento DIV vazio à página onde deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois ela é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   Verifique se o recurso de tela cheia funciona corretamente no Internet Explorer. Verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento superior à do espaço reservado DIV.

   A seguir está um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Definição do tamanho do visualizador

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Em sistemas desktop, as miniaturas são colocadas abaixo da visualização principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando a API `setAsset()`. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na parte inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e deixar a visualização principal aumentar sua altura e ocupar a área de miniaturas. Ou, você pode manter o tamanho da visualização principal estático e recolher a área do visualizador externo, permitindo que o conteúdo da página da Web se mova para cima e, em seguida, usar o espaço livre da página que fica das miniaturas.

   Para manter os limites do visualizador externo intactos, defina o tamanho para `.s7mixedmediaviewer` classe CSS de nível superior em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic, ou passado explicitamente usando o comando style.

   Consulte [Personalizando o visualizador de mídia mista](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir o tamanho do visualizador externo estático em uma página HTML:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na seguinte página de amostra. Observe que quando você alterna entre os conjuntos, o tamanho do visualizador externo não muda:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Para tornar as dimensões de visualização principais estáticas, defina o tamanho do visualizador em unidades absolutas para o componente SDK interno `Container` usando o seletor CSS `.s7mixedmediaviewer .s7container` ou usando o modificador `stagesize`.

   A seguir está um exemplo de como definir o tamanho do visualizador para o componente SDK interno `Container` para que a área de visualização principal não altere seu tamanho ao alternar o ativo:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de amostra a seguir mostra o comportamento do visualizador com um tamanho de visualização principal fixo. Observe que quando você alterna entre os conjuntos, a visualização principal permanece estática e o conteúdo da página da Web se move verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Você pode definir o modificador `stagesize` no registro predefinido do visualizador no Dynamic Media Classic, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params`, ou como uma chamada de API conforme descrito na seção Referência de Comando desta Ajuda, como a seguir:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.MixedMediaViewer`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem passado como propriedade `serverUrl`, o URL do servidor de vídeo passado como propriedade `videoserverurl` e ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o método `init()` logo antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. O exemplo supõe que `mixedMediaViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagens; [!DNL http://s7d1.scene7.com/is/content/] é o URL do servidor de vídeo; e [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] é o ativo:

```
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

O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de mídia mista com um tamanho fixo:

```
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

## Incorporação responsiva com altura sem restrições {#section-056cb574713c4d07be6d07cf3c598839}

Com incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita que o container do visualizador `DIV` tome 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web se parece com o seguinte:

```
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

Adicionar o visualizador a uma página assim é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o DIV do container.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o DIV do container ao DIV `"holder"` existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura irrestrita:

[Demos ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Incorporação flexível de tamanho com largura e altura definidas {#section-0a329016f9414d199039776645c693de}

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%.

```
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

O restante das etapas de incorporação são idênticos às etapas usadas para incorporação de design responsivo com altura irrestrita. O exemplo resultante é o seguinte:

```
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

## Incorporação usando a API baseada em Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()`, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

