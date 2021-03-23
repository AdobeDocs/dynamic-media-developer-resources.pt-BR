---
description: Visualizador de zoom é um visualizador de imagem que exibe uma imagem com zoom. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele tem ferramentas de zoom, suporte de tela cheia, amostras e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
seo-description: Visualizador de zoom é um visualizador de imagem que exibe uma imagem com zoom. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele tem ferramentas de zoom, suporte de tela cheia, amostras e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.
seo-title: Zoom
solution: Experience Manager
title: Zoom
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2471'
ht-degree: 0%

---


# Zoom{#zoom}

Visualizador de zoom é um visualizador de imagem que exibe uma imagem com zoom. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele tem ferramentas de zoom, suporte de tela cheia, amostras e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador.

Tipo de visualizador 502.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Uso do Visualizador de Zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de Zoom representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de Zoom no modo pop-up usando uma página HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e o esfolamento são semelhantes aos dos outros visualizadores. Todo o esfolamento é obtido por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de Zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador de zoom é compatível com os seguintes gestos de toque, comuns em outros aplicativos móveis. Quando o visualizador não consegue processar o gesto de deslizamento do usuário, ele encaminha o evento para o navegador da Web para executar a rolagem da página nativa. Esse tipo de funcionalidade permite que o usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área da tela do dispositivo.

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
   <td colname="col2"> <p> Seleciona uma nova miniatura em amostras. Na exibição principal, oculta ou revela elementos da interface do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque duplo </p> </td> 
   <td colname="col2"> <p> Aumenta o zoom em um nível até atingir a ampliação máxima. O próximo gesto de toque duplo redefine o visualizador para o estado de visualização inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinça </p> </td> 
   <td colname="col2"> <p>Aumenta ou diminui o zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque ou cintilação horizontal </p> </td> 
   <td colname="col2"> <p> Percorre a lista de amostras na barra de amostras. </p> <p> Se a imagem estiver em um estado de redefinição e o parâmetro <span class="codeph"> de transição de estrutura </span> for definido como slide, o ativo será alterado com a animação de slide. Para outros modos <span class="codeph"> de transição de estrutura </span>, o gesto executa a rolagem de página nativa. </p> <p> Se a imagem estiver ampliada, ela move a imagem na horizontal. Se a imagem for movida para a borda da exibição e um deslizamento for executado na mesma direção, o gesto executará a rolagem da página nativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passagem vertical </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, o gesto executará a rolagem da página nativa. </p> <p> Quando a imagem é ampliada, ela move a imagem verticalmente. Se a imagem for movida para a borda da exibição e um deslizamento for executado na mesma direção, o gesto executará a rolagem da página nativa. </p> <p> Se o gesto for feito dentro da área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador aceita entrada de toque e entrada de mouse em dispositivos Windows com uma tela sensível ao toque e um mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Esse visualizador é totalmente acessível por teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando Visualizador de Zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter layout estático ou usar design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada `window.open()` do JavaScript, o elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML pronta para uso no modo de operação pop-up. A página HTML pronta para uso é chamada `ZoomViewer.html` e está localizada na subpasta `html5/` da implantação padrão do IS-Viewers, como no exemplo a seguir:

`<s7viewers_root>/html5/ZoomViewer.html`

Aplique CSS personalizado para obter uma aparência personalizada para a página.

Este é um exemplo de código HTML que abre o visualizador na nova janela:

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. Normalmente, o visualizador ocupa apenas parte do imóvel da página.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, além de páginas projetadas responsivas que ajustam o layout automaticamente, dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor opção para páginas da Web com layout estático.

O modo de incorporação de design responsivo supõe que o redimensionamento do visualizador é necessário durante o tempo de execução devido à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir apenas a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa lógica garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas, como Bootstrap, Foundation e assim por diante.

Se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá essa área e seguirá o tamanho fornecido pela página da Web. Por exemplo, incorporar o visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

## Incorporação de tamanho fixo {#section-44f365e6c0dd40709467a459afa82a7f}

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, inclua [!DNL ZoomViewer.js]. O arquivo [!DNL ZoomViewer.js] está localizado na subpasta [!DNL html5/js/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic que tenham os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript `include` do visualizador principal na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador em tempo de execução. Em particular, não faça referência diretamente à biblioteca de SDK `Utils.js` HTML5 carregada pelo visualizador do `/s7viewers` caminho de contexto (o chamado SDK consolidado `include`). O motivo é que o local de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciado pela lógica do visualizador e o local muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão de produto for implantada.

1. Definição do DIV do contêiner.

   Adicione um elemento DIV vazio à página onde você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador.

   O DIV de espaço reservado é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Este é um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens, em sistemas de desktop as miniaturas são colocadas abaixo da exibição principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal em tempo de execução usando `setAsset()` API. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na parte inferior, quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e permitir que a exibição principal aumente sua altura e ocupe a área de miniaturas. Ou, você pode manter o tamanho da exibição principal estático e recolher a área do visualizador externo, permitindo que o conteúdo da página da Web se mova para cima e usar o espaço real de tela livre remanescente das miniaturas.

   Para manter os limites do visualizador externo intactos, defina o tamanho para a classe CSS de nível superior `.s7zoomviewer` em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou passado explicitamente usando um comando style.

   Consulte [Personalizando visualizador de zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador externo estático na página HTML:

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com um visualizador externo fixo no exemplo a seguir. Observe que, quando você alternar entre conjuntos, o tamanho do visualizador externo não é alterado:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   Para tornar as dimensões de visualização principais estáticas, defina o tamanho do visualizador em unidades absolutas para o componente SDK interno `Container` usando o seletor de CSS `.s7zoomviewer` `.s7container` ou usando o modificador `stagesize`.

   Este é um exemplo de definição do tamanho do visualizador para o componente interno do SDK `Container` para que a área de visualização principal não altere seu tamanho ao alternar o ativo:

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de demonstração a seguir mostra o comportamento do visualizador com um tamanho de exibição principal fixo. Observe que, ao alternar entre conjuntos, a exibição principal permanece estática e o conteúdo da página da Web se move verticalmente.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   Você pode definir o modificador `stagesize` no registro de predefinição do visualizador no Dynamic Media Classic, ou pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de comandos desta Ajuda, como em:

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Após concluir as etapas acima, crie uma instância de `s7viewers.ZoomViewer` classe, passe todas as informações de configuração para seu construtor e chame o método `init()` em uma instância do visualizador.

   As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do contêiner do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de Exibição de Imagem passado como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame o método `init()` antes de fechar a tag `BODY` ou no evento body `onload()` .

   Ao mesmo tempo, o elemento do contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando o método `init()`. Este exemplo supõe que `zoomViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado DIV, `http://s7d1.scene7.com/is/image/` é o URL de disponibilização de imagens e `Scene7SharedAssets/ImageSet-Views-Sample` é o ativo.

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de vídeo com um tamanho fixo:

   ```
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

## Incorporação de design responsivo com altura sem restrições {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Com a incorporação responsiva do design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho de tempo de execução do contêiner do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita que o contêiner do visualizador `DIV` pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o DIV do contêiner ao DIV `"holder"` existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporação de tamanho flexível com largura e altura definidas {#section-3674e6c032594441a6576b7fb1de6e64}

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ela fornece ambos os tamanhos para o `"holder"` DIV e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%.

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

O restante das etapas de incorporação são idênticas às etapas usadas para incorporação de design responsivo com altura irrestrita. O exemplo resultante é o seguinte:

```
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

## Como incorporar usando a API baseada em setter {#section-44e014925f24418b900696003855c0a9}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não utiliza parâmetros e parâmetros de configuração são especificados usando `setContainerId()`, `setParam()` e `setAsset()` métodos de API com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

