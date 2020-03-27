---
description: O Visualizador de zoom incorporado é um visualizador de imagens. Ele exibe uma imagem estática com a versão ampliada mostrada sobre a imagem estática quando um usuário passa o mouse sobre ela ou toca a visualização principal. Este visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsive
seo-description: O Visualizador de zoom incorporado é um visualizador de imagens. Ele exibe uma imagem estática com a versão ampliada mostrada sobre a imagem estática quando um usuário passa o mouse sobre ela ou toca a visualização principal. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.
seo-title: Zoom em linha
solution: Experience Manager
title: Zoom em linha
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Zoom em linha{#inline-zoom}

O Visualizador de zoom incorporado é um visualizador de imagens. Ele exibe uma imagem estática com a versão ampliada mostrada sobre a imagem estática quando um usuário passa o mouse sobre ela ou toca a visualização principal. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador.

O tipo de visualizador é 504.

Consulte Requisitos [do sistema e pré-requisitos](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400)

## Uso do Visualizador de zoom incorporado {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de zoom incorporado representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador no tempo de execução.

O Visualizador de zoom em linha pode ser usado no modo pop-up usando a página HTML pronta para produção fornecida com Visualizadores do Servidor de imagens ou no modo incorporado, onde é integrado a uma página da Web de público alvo usando a API documentada.

A configuração e a capa são semelhantes às dos outros visualizadores. Você pode usar CSS personalizado para aplicar capas.

Consulte Referência de [comando comum a todos os visualizadores - Referência de atributos](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuração e [comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador de zoom incorporado {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de zoom incorporado oferece suporte a gestos de toque único e multitoque comuns em outros aplicativos móveis.

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
   <td colname="col2"> <p> Ativa a visualização de flyout ou altera o nível de zoom primário e secundário em amostras, seleciona a nova miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque horizontal ou toque </p> </td> 
   <td colname="col2"> <p> Percorre a lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque vertical </p> </td> 
   <td colname="col2"> <p>Se o gesto for feito dentro da área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada de toque e à entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Este visualizador está totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)do teclado.

## Incorporando o Visualizador de zoom incorporado {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link clicável que abre o visualizador em uma janela separada do navegador. Em outros casos, pode ser necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes, ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva.

**Pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta quando a janela do navegador é redimensionada ou a orientação do dispositivo é alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada `window.open()` JavaScript, o elemento `A` HTML configurado corretamente ou qualquer outra forma adequada.

É recomendável usar a página HTML predefinida para o modo pop-up chamado `FlyoutViewer.html`. Ele está localizado na [!DNL html5/] subpasta da implantação padrão do Servidor de imagens - Visualizadores:

`<s7viewers_root>/html5/FlyoutViewer.html`

Também é necessário ter o componente FlyoutZoomView configurado para funcionar no modo de zoom em linha. É recomendável usar a predefinição `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` predefinida para o visualizador de zoom incorporado ou uma predefinição personalizada derivada dele. A personalização visual pode ser alcançada pela aplicação de CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incorporação de tamanho fixo e incorporação responsiva**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio da página da Web.

O caso de uso principal são as páginas da Web orientadas para desktops ou tablets, e também as páginas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

O modo de incorporação de tamanho fixo é usado quando o visualizador não altera seu tamanho após a carga inicial. Essa opção é melhor para páginas da Web que tenham um layout de página estático.

O modo de incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado durante o tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

Ao usar o modo de incorporação de design responsivo com o Visualizador de zoom incorporado, certifique-se de especificar pontos de interrupção explícitos para a imagem de visualização principal usando o `imagereload` parâmetro. Idealmente, combine seus pontos de interrupção com os pontos de interrupção da largura do visualizador, conforme indicado pelo CSS da página da Web.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como uma página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Isso significa que o ativo se encaixa perfeitamente na visualização, sem qualquer preenchimento lateral. Esse caso de uso em particular é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá somente essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo de caso de uso é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de poder usar a API do visualizador, verifique se você incluiu `FlyoutViewer.js`. `FlyoutViewer.js` está localizado na seguinte [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Scene7 e ele for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Scene7 com os IS-Viewers instalados.

Um caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal na sua página. `include` Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à `Utils.js` biblioteca do SDK HTML5 carregada pelo visualizador a partir do caminho de `/s7viewers` contexto (o chamado SDK consolidado `include`). O motivo é que a localização das bibliotecas do visualizador do tempo de execução `Utils.js` ou semelhantes é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. A Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o DIV do container.

   Adicione um elemento DIV vazio à página onde deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   É responsabilidade da página da Web especificar a propriedade adequada `z-index` para o elemento DIV de espaço reservado. Isso garante que a parte de flyout do visualizador apareça na parte superior dos outros elementos da página da Web.

   A seguir está um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Definição do tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Em sistemas desktop, as miniaturas são colocadas abaixo da visualização principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando a `setAsset()` API. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na área inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e deixar a visualização principal aumentar sua altura e ocupar a área de miniaturas. Ou você pode manter o tamanho da visualização principal estático e reduzir a área do visualizador externo, permitindo, assim, que o conteúdo da página da Web se mova para cima e, em seguida, usar o espaço livre da página nas miniaturas.

   Para manter os limites do visualizador externo intactos, defina o tamanho para a classe CSS de nível superior em unidades absolutas. `.s7flyoutviewer` O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Scene7 Publishing System, ou transmitido explicitamente usando o comando style.

   Consulte [Personalização do Visualizador](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) de zoom incorporado para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir o tamanho do visualizador externo estático em uma página HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na seguinte página de amostra. Observe que quando você alterna entre os conjuntos, o tamanho do visualizador externo não muda:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   Para tornar as dimensões principais da visualização estáticas, defina o tamanho do visualizador em unidades absolutas para o componente interno do `Container` SDK usando o seletor de `.s7flyoutviewer .s7container` CSS. Além disso, você deve substituir o tamanho fixo definido para a classe CSS de `.s7flyoutviewer` nível superior no CSS do visualizador padrão, definindo-o como `auto`.

   A seguir está um exemplo de como definir o tamanho do visualizador para o componente interno do `Container` SDK para que a área de visualização principal não altere seu tamanho ao alternar o ativo:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de amostra a seguir mostra o comportamento do visualizador com um tamanho de visualização principal fixo. Observe que quando você alterna entre os conjuntos, a visualização principal permanece estática e o conteúdo da página da Web se move verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   Além disso, observe que o CSS do visualizador padrão fornece um tamanho fixo para sua área externa pronta para uso.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.FlyoutViewer` classe, passe todas as informações de configuração para o construtor e chame o `init()` método em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o `containerId` `params` campo que contém o nome da ID do container do visualizador e o objeto JSON aninhado com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o `params` objeto deve ter pelo menos o URL de disponibilização de imagem passado como `serverUrl` propriedade, o ativo inicial como `asset` parâmetro, caminho base para carregar CSS como `contentUrl` parâmetro e nome predefinido como `config` parâmetro. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o `init()` método imediatamente antes da `BODY` tag de fechamento ou no `onload()` evento body.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o `init()` método. O exemplo supõe que `inlineZoomViewer` seja a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` é o URL de disponibilização de imagem; e `Scene7SharedAssets/ImageSet-Views-Sample` é o ativo:

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de zoom em linha com um tamanho fixo:

   ```
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

## Incorporação de design responsivo com altura irrestrita {#section-056cb574713c4d07be6d07cf3c598839}

Com incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita que o container do visualizador pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. `DIV` O código HTML da página da Web se parece com o seguinte:

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

Adicionar o visualizador a uma página assim é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você precisa substituir o dimensionamento fixo do CSS do visualizador padrão pelo tamanho definido em unidades relativas.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo com as três exceções a seguir:

* adicionar o container `DIV` ao &quot;titular&quot; existente `DIV`;
* parâmetro adicionado `imagereload` com pontos de interrupção explícitos;
* em vez de definir um tamanho fixo do visualizador usando unidades absolutas, use o CSS que define o visualizador `width` e `height` para 100%, como a seguir:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura sem restrições:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## Incorporação flexível de tamanho com definição de largura e altura {#section-0a329016f9414d199039776645c693de}

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Fornece ambos os tamanhos para o `"holder"` DIV e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%.

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

## Como incorporar usando a API baseada em Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando métodos `setContainerId()`, `setParam()`e `setAsset()` API, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

