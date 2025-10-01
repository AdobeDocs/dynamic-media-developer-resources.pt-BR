---
title: Zoom básico
description: O Visualizador de zoom básico é um visualizador de imagens que exibe uma única imagem com zoom. Ele tem ferramentas de zoom, suporte para tela cheia e um botão de fechamento opcional. Este visualizador é o mais leve. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ee15ce21-20c4-428b-9512-050115e4c322
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1998'
ht-degree: 0%

---

# Zoom básico{#basic-zoom}

O Visualizador de zoom básico é um visualizador de imagens que exibe uma única imagem com zoom. Ele tem ferramentas de zoom, suporte para tela cheia e um botão de fechamento opcional. Este visualizador é o mais leve. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são compatíveis com esse visualizador.

Visualizador tipo 501.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Usando o Visualizador de Zoom Básico {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de zoom básico representa um arquivo do JavaScript e um conjunto de arquivos auxiliares que o visualizador baixa no tempo de execução. Basicamente, é uma inclusão única do JavaScript com todos os componentes do Viewer SDK usados por esse visualizador, ativos e CSS específicos.

Você pode usar o Visualizador de zoom básico no modo pop-up usando uma página do HTML pronta para produção fornecida com Visualizadores IS ou no modo incorporado, onde ela é integrada à página da Web de destino usando a API documentada.

A configuração e a aparência são semelhantes às dos outros visualizadores. Toda a atribuição de capa é obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de zoom básico {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador de zoom básico é compatível com os seguintes gestos de toque, comuns em outros aplicativos móveis.

Quando o visualizador não consegue processar o gesto de deslizar de um usuário, ele encaminha o evento para o navegador da Web para executar uma rolagem de página nativa. Esse tipo de funcionalidade permite que o usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área da tela do dispositivo.

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
   <td colname="col2"> <p>Oculta ou revela elementos da interface do usuário. </p> </td> 
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
   <td colname="col1"> <p>Deslizar </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, o gesto executará uma rolagem de página nativa. </p> <p> Quando o zoom da imagem é ampliado, ela move a imagem. Se a imagem for movida para a borda da exibição e um deslizamento for executado nessa direção, o gesto executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada por toque e à entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de zoom básico {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador é compatível com três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento do HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML pronta para uso para o modo de operação pop-up. Nesse caso, ele é chamado de [!DNL BasicZoomViewer.html] e está localizado na subpasta [!DNL html5/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Veja a seguir um exemplo do código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio imobiliário de uma página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação de design responsivo presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de design da Web, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho do HTML. Antes de usar a API do visualizador, inclua [!DNL BasicZoomViewer.js]. O arquivo [!DNL BasicZoomViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do HTML5 SDK carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, a inserção de uma referência direta a qualquer JavaScript `include` secundário usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do container DIV.

   Adicione um elemento DIV vazio à página em que você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio de CSS.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7basiczoomviewer` em unidades absolutas ou usando o modificador `stagesize`.

   Coloque o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado. Posteriormente, ele é atribuído a um registro de predefinição do visualizador no Dynamic Media Classic ou passado explicitamente usando um comando de estilo.

   Consulte [Personalizando o visualizador de zoom básico](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página do HTML:

   ```html {.line-numbers}
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro de predefinição do visualizador no Dynamic Media Classic. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou, como uma chamada de API, conforme descrito na seção Referência de Comandos, da seguinte maneira:

   ```html {.line-numbers}
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.BasicZoomViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter um campo containerId que contenha o nome do visualizador `container ID` e do objeto JSON `params` aninhado com parâmetros de configuração com suporte do visualizador. Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl`, e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando esse evento ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. O exemplo considera `basicZoomViewer` como a instância do visualizador; `s7viewer` como o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` como a URL do Servidor de Imagens e `Scene7SharedAssets/Backpack_B` como o ativo:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de zoom básico com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporação responsiva de design com altura irrestrita**

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

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que não é necessário definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicione o contêiner DIV ao `"holder"` DIV existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Inserção de tamanho flexível com Largura e Altura Definidas**

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

O restante das etapas de incorporação são idênticas às etapas usadas para incorporação responsiva com altura irrestrita. O exemplo resultante é o seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporando Usando API baseada em Setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```
