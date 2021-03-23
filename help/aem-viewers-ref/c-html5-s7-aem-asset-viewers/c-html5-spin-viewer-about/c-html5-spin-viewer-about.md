---
description: Visualizador de rotação é um visualizador de imagem que fornece uma visualização de 360 graus da imagem ou até mesmo uma visualização multidimensional se um conjunto de rotação apropriado estiver sendo usado. Ele tem ferramentas de zoom e rotação, suporte de tela cheia e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
seo-description: Visualizador de rotação é um visualizador de imagem que fornece uma visualização de 360 graus da imagem ou até mesmo uma visualização multidimensional se um conjunto de rotação apropriado estiver sendo usado. Ele tem ferramentas de zoom e rotação, suporte de tela cheia e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.
seo-title: Rotação
solution: Experience Manager
title: Rotação
uuid: 5d5cdf83-cfe8-48cd-af74-b270f7400b14
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---


# Rotação{#spin}

Visualizador de rotação é um visualizador de imagem que fornece uma visualização de 360 graus da imagem ou até mesmo uma visualização multidimensional se um conjunto de rotação apropriado estiver sendo usado. Ele tem ferramentas de zoom e rotação, suporte de tela cheia e um botão de fechamento opcional. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador.

Tipo de visualizador 503.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Uso do Visualizador de rotação {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de rotação representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Visualizador de rotação pode ser usado no modo pop-up usando a página HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e o esfolamento são semelhantes aos dos outros visualizadores. Toda a definição de skins pode ser alcançada por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de rotação {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador de rotação é compatível com os seguintes gestos de toque que são comuns em outros aplicativos móveis. Quando o visualizador não consegue processar o gesto de deslizamento de um usuário, ele encaminha o evento para o navegador da Web para executar uma rolagem de página nativa. Isso permite que o usuário navegue pela página mesmo se o visualizador ocupar a maior parte da área da tela do dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Toque duplo </p> </td> 
   <td colname="col2"> <p> Aumenta o zoom em um nível até atingir a ampliação máxima. O próximo gesto de toque duplo redefine o visualizador para o estado de visualização inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinça </p> </td> 
   <td colname="col2"> <p>Aumenta ou diminui o zoom da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque ou cintilação horizontal </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, ela girará através do conjunto horizontalmente. </p> <p> Se a imagem estiver ampliada, ela move a imagem na horizontal. Se a imagem for movida para a borda da exibição e um deslizamento ainda for feito nessa direção, o gesto executará uma rolagem de página nativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou piscar na vertical </p> </td> 
   <td colname="col2"> <p> Se a imagem estiver em um estado de redefinição, ela alterará o ângulo de exibição vertical caso um conjunto de rotação multidimensional seja usado. Em um conjunto de rotação unidimensional, ou quando um conjunto de rotação multidimensional está no último ou no primeiro eixo, para que o deslizamento vertical não resulte em uma alteração no ângulo de exibição vertical, o gesto executa uma rolagem de página nativa. </p> <p> Se a imagem estiver ampliada, ela moverá a imagem verticalmente. Se a imagem for movida para a borda da exibição e um deslizamento ainda for feito nessa direção, o gesto executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O visualizador também suporta entrada de toque e entrada de mouse em dispositivos Windows com tela de toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Esse visualizador é totalmente acessível por teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando Visualizador de rotação {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação de um dispositivo móvel seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada `window.open()` do JavaScript, o elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML pronta para uso no modo de operação pop-up. Nesse caso, ele é chamado [!DNL SpinViewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas parte do imóvel de uma página da web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, e também páginas de design responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva de design supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo pode ser a incorporação do visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o Visualizador de rotação a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, inclua `SpinViewer.js`. `SpinViewer.js` está localizado na  [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media que têm os IS-Viewers instalados.

   O caminho relativo tem a seguinte aparência:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
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

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7spinviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento em CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic, ou passado explicitamente usando um comando style.

   Consulte [Personalizando o Visualizador de rotação](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro de predefinição do visualizador no Dynamic Media Classic, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API conforme descrito na seção Referência de comandos, como o seguinte:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Após concluir as etapas acima, crie uma instância de `s7viewers.SpinViewer` classe, passe todas as informações de configuração para seu construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto tem `containerId` campo que contém o nome da ID do contêiner do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador. Nesse caso de objeto `params`, ele deve ter pelo menos o URL de Exibição de Imagem passado como propriedade `serverUrl` e ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame o método `init()` antes de fechar a tag `BODY` ou no evento body `onload()` .

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando o método `init()`. O exemplo assume que `spinViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagem e [!DNL Scene7SharedAssets/SpinSet_Sample] é o ativo.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de rotação com um tamanho fixo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação responsiva do design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho de tempo de execução do contêiner do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita que o contêiner do visualizador `DIV` pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web resultante é semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante à incorporação de tamanho fixo, com a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com incorporação de tamanho fixo. Adicione o contêiner `DIV` ao &quot; detentor&quot; existente `DIV`. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra casos de uso mais reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporação flexível de tamanho com largura e altura definidas**

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ou seja, ele fornece ambos os tamanhos ao &quot; holder&quot; `DIV` e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%:

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

As etapas de incorporação restantes são idênticas à incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com esse construtor de API, não utiliza parâmetros e os parâmetros de configuração são especificados usando `setContainerId()`, `setParam()` e `setAsset()` métodos de API com chamadas JavaScript separadas.

O exemplo a seguir mostra a incorporação de tamanho fixo com a API baseada em setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```

