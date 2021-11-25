---
title: Visualizador panorâmico
description: HTML5 Panorâmica Viewer é um visualizador de imagens que exibe uma imagem panorâmica. O objetivo desse visualizador é exibir um panorama esférico, também conhecido como imagem equidirecional. Suporta o deslocamento automático e o deslocamento por movimentos giroscópicos.  Ele foi projetado para funcionar em desktops e dispositivos móveis.  O modo de visualização de realidade virtual está disponível no suporte a dispositivos móveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 959089682d432a72b1860f2180daac7de0afedf2
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 0%

---

# Panorâmica{#panoramic}

HTML5 Panorâmica Viewer é um visualizador de imagens que exibe uma imagem panorâmica. O objetivo desse visualizador é exibir um panorama esférico, também conhecido como imagem equidirecional. Suporta o deslocamento automático e o deslocamento por movimentos giroscópicos.  Ele foi projetado para funcionar em desktops e dispositivos móveis.  O modo de visualização de realidade virtual está disponível no suporte a dispositivos móveis.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Tipo de visualizador 514.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Uso do Visualizador panorâmico {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Visualizador panorâmico representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão JavaScript com todos os componentes do SDK do visualizador HTML5 usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.
HTML5 O Visualizador panorâmico pode ser usado no modo pop-up usando a página HTML pronta para produção fornecida com os IS-Viewers ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.
A configuração e o esfolamento são semelhantes aos dos outros visualizadores do HTML5. Toda a definição de skins pode ser alcançada por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador Panorâmico do HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 O Visualizador panorâmico é compatível com o deslocamento automático e a navegação por arrastar ou girescópio.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navegação </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Desktop </p> </td> 
   <td colname="col2"> <p>Faça o deslocamento automático e arraste para navegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo de toque </p> </td> 
   <td colname="col2"> <p>Deslocar e arrastar automaticamente para navegar por padrão. Navegue pelo movimento giroscópico no modo de renderização VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador aceita entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.
O Visualizador panorâmico tem a capacidade de renderizar imagens panorâmicas no modo de Realidade Virtual (VR) especificando o modificador de renderização.  Quando a renderização estiver ativada, uma imagem panorâmica será exibida em telas divididas.  Um caso de uso comum seria servir a imagem em um celular montado em um fone de ouvido de realidade virtual, fornecendo imagens separadas para cada olho.  O visualizador responderá ao movimento giroscópico da cabeça e navegará pela imagem.

## Incorporando o Visualizador Panorâmico do HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornecerá um link e, ao clicar nesse link, o visualizador será aberto em uma janela separada do navegador. Em outros casos, pode ser necessário incorporar o visualizador diretamente na página de hospedagem. Neste último caso, a página da Web pode ter layout estático ou ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada window.open() do JavaScript, um elemento HTML corretamente configurado ou qualquer outra maneira adequada.

É recomendável usar uma página de HTML pronta para uso no modo de operação pop-up. É chamado de [!DNL PanoramicViewer.html] e está localizado sob a [!DNL html5/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

A personalização visual pode ser alcançada com a aplicação de CSS personalizado.

Este é um exemplo de HTML code que abre o visualizador na nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. Normalmente, o visualizador ocupa apenas uma parte do espaço da página web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, e também páginas da Web responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva supõe que o visualizador talvez precise ser redimensionado em tempo de execução em resposta à alteração de tamanho do DIV do contêiner. O caso de uso mais comum é adicionar visualizador a uma página da Web que use um layout flexível.

No modo responsivo, o visualizador se comportará de forma diferente dependendo da maneira como a página da Web dimensiona o DIV do contêiner. Se a página da Web definir apenas a largura do DIV do contêiner, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo que está sendo usado; isso garantirá que o ativo esteja perfeitamente encaixado na exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do DIV do contêiner do visualizador, o visualizador apenas preencherá essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo pode ser a incorporação do visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.


**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no HTML head. Antes de usar a API do visualizador, verifique se você incluiu [!DNL PanoramicViewer.js]. O [!DNL PanoramicViewer.js] O arquivo está localizado sob a variável [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores da Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores da Adobe Dynamic Media Classic que têm os IS-Viewers instalados.

O caminho relativo é semelhante ao seguinte:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Referencie somente o JavaScript do visualizador principal `include` na sua página. Não faça referência a arquivos JavaScript adicionais no código da página da Web que possam ser baixados pela lógica do visualizador em tempo de execução. Em particular, não faça referência diretamente ao SDK do HTML5 `Utils.js` biblioteca carregada pelo visualizador de `/s7viewers` caminho do contexto (o chamado SDK consolidado) `include`). O motivo é que a localização da variável `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução são totalmente gerenciadas pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página, interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do DIV do contêiner.

   Adicione um elemento DIV vazio à página onde você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado DIV é um elemento posicionado, o que significa que a variável `position` A propriedade CSS está definida como `relative` ou `absolute`.


   Este é um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7panoramicviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   O dimensionamento no CSS pode ser colocado diretamente na página HTML ou no arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no AOD ou passado explicitamente usando o comando style. Consulte Personalização da seção Visualizador para obter mais informações sobre como estilizar o visualizador com CSS. Veja abaixo um exemplo de definição do tamanho estático do visualizador em HTML page:

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` O modificador pode ser transmitido explicitamente com o código de inicialização do visualizador com a coleção de parâmetros ou como uma chamada de API, conforme descrito na seção Referência de comandos , desta forma:

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   A abordagem baseada em CSS é recomendada e será usada neste exemplo.


1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.PanoramicViewer` classe , passe todas as informações de configuração para seu construtor e chame `init(`) em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo containerId que contém o nome da ID do contêiner do visualizador e o objeto JSON de parâmetros aninhados com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto params deve ter pelo menos o URL de Exibição de Imagem passado como `serverUrl` propriedade e ativo inicial como parâmetro de ativo. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame a função `init()` método antes de fechar `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, pode estar oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando a função `init()` método . Este exemplo supõe `panoramicViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagens e [!DNL Scene7SharedAssets/PanoramicImage-Sample] é o ativo.

   ```
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de panorâmica com um tamanho fixo:

   ```
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação responsiva, a página da Web normalmente tem algum tipo de layout flexível em vigor, que determina o tamanho do tempo de execução do DIV do contêiner do visualizador. Para as finalidades deste exemplo, vamos supor que a página da Web permite que o DIV do contêiner do visualizador pegue 80% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código de HTML da página da Web pode ser semelhante a:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

Adicionar o visualizador a essa página é muito semelhante à incorporação de tamanho fixo, com a única diferença de que você não precisa definir explicitamente o tamanho do visualizador:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. O DIV do contentor deve ser adicionado ao DIV do &quot;titular&quot; existente. O código a seguir é um exemplo completo, você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

A página de exemplos a seguir ilustra o uso mais real da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Localização de demonstração alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporação de design responsivo com largura e altura definidas**

Se houver incorporação de design responsivo com largura e altura definidas, o estilo da página da Web será diferente; fornece ambos os tamanhos ao &quot; detentor&quot; `DIV` e centralize-o na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%:

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

O restante das etapas de incorporação são idênticas à incorporação responsiva com altura irrestrita. O exemplo resultante é

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com essa API, o construtor não utiliza parâmetros e parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`e `setAsset()` Métodos de API com chamadas JavaScript separadas.

O exemplo a seguir ilustra a incorporação de tamanho fixo com a API baseada em setter:

```
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
