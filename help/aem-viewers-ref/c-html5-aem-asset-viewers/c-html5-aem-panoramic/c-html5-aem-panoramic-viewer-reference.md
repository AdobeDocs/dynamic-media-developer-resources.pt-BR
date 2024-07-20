---
title: Visualizador panorâmico
description: HTML5 Panoramic Viewer é um visualizador de imagens que exibe uma imagem panorâmica. A finalidade deste visualizador é exibir um panorama esférico, também conhecido como imagem equiretangular. Suporta o movimento panorâmico automático e panorâmico por movimento giroscópico. Ele foi projetado para funcionar em desktops e dispositivos móveis. O modo de visualização de realidade virtual está disponível em dispositivos móveis compatíveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# Panorâmica{#panoramic}

HTML5 Panoramic Viewer é um visualizador de imagens que exibe uma imagem panorâmica. A finalidade deste visualizador é exibir um panorama esférico, também conhecido como imagem equiretangular. Suporta o movimento panorâmico automático e panorâmico por movimento giroscópico. Ele foi projetado para funcionar em desktops e dispositivos móveis. O modo de visualização de realidade virtual está disponível em dispositivos móveis compatíveis.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Visualizador tipo 514.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Uso do Visualizador Panorâmico {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador panorâmico do HTML5 representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares baixados pelo visualizador no tempo de execução. O conjunto de arquivos auxiliares é uma única inclusão do JavaScript com todos os componentes do SDK do Visualizador de HTML5 usados por esse visualizador específico, ativos, CSS.
O Visualizador panorâmico do HTML5 pode ser usado no modo pop-up usando a página de HTML pronta para produção fornecida com os Visualizadores IS ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.
A configuração e a aparência são semelhantes às dos outros visualizadores do HTML5. Toda a atribuição de capa pode ser obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador Panorâmico do HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador panorâmico do HTML5 suporta panorama automático e navegação por arrastar ou movimento giroscópico.

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
   <td colname="col2"> <p>Desloque-se automaticamente e arraste para navegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo de toque </p> </td> 
   <td colname="col2"> <p>Deslocar automaticamente e arrastar para navegar por padrão. Navegar por movimento giroscópico no modo de renderização VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador é compatível com entrada por toque e entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.
O Visualizador panorâmico pode renderizar imagens panorâmicas no modo Realidade Virtual (VR) especificando o modificador vrrender. Quando o vrrender está ativado, uma imagem panorâmica é exibida em telas divididas. Um caso de uso comum seria veicular a imagem em um celular montado em um headset de realidade virtual, fornecendo imagens separadas para cada olho. O visualizador responde ao movimento giroscópico da cabeça e navega pela imagem.

## Incorporando o Visualizador Panorâmico do HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link. Selecionar esse link abre o visualizador em uma janela separada do navegador. Em outros casos, pode ser necessário incorporar o visualizador na página de hospedagem. No último caso, a página da Web pode ter layout estático ou ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento A HTML configurado corretamente ou qualquer outra maneira adequada.

É recomendável usar uma página de HTML para o modo de operação pop-up. Ele é chamado de [!DNL PanoramicViewer.html] e está localizado na subpasta [!DNL html5/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

A personalização visual pode ser obtida ao aplicar CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador na nova janela:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do espaço físico da página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas da Web responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu container DIV. O caso de uso mais comum é a adição do visualizador a uma página da Web que usa layout flexível.

No modo responsivo, o visualizador se comporta de forma diferente dependendo da forma como a página da Web dimensiona seu container DIV. Se a página da Web definir somente a largura do contêiner DIV, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Esse método garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas, como Bootstrap, Foundation e outras.

Caso contrário, se a página da Web definir a largura e a altura para o container DIV do visualizador, o visualizador preencherá essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua [!DNL PanoramicViewer.js]. O arquivo [!DNL PanoramicViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do SDK HTML5 carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
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

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7panoramicviewer` em unidades absolutas ou usando o modificador `stagesize`.

   O dimensionamento no CSS pode ser colocado diretamente na página do HTML ou no arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no AOD ou passado explicitamente usando o comando style. Consulte a seção Personalização do visualizador para obter mais informações sobre como estilizar o visualizador com CSS. Veja abaixo um exemplo de definição do tamanho do visualizador estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   O modificador `stagesize` pode ser passado explicitamente com o código de inicialização do visualizador com a coleção params ou como uma chamada de API, conforme descrito na seção Referência de Comando, desta forma:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   A abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.PanoramicViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init(` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo containerId, que contém o nome da ID do contêiner do visualizador e o objeto JSON de parâmetros aninhados com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto params deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl` e o ativo inicial como parâmetro do ativo. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. Este exemplo supõe que `panoramicViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é a URL do Servidor de Imagens e [!DNL Scene7SharedAssets/PanoramicImage-Sample] é o ativo.

   ```html {.line-numbers}
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

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador panorâmico com um tamanho fixo:

   ```html {.line-numbers}
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

**Incorporação responsiva de design com altura irrestrita**

Com a incorporação responsiva, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do container do visualizador DIV. Para os fins deste exemplo, vamos supor que a página da Web permita que o container do visualizador DIV ocupe 80% do tamanho da janela do navegador da Web, deixando sua altura irrestrita. O código de HTML da página da Web pode ser semelhante a:

```html {.line-numbers}
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

Adicionar o visualizador a essa página é semelhante à incorporação de tamanho fixo, com a única diferença de que você não precisa definir explicitamente o tamanho do visualizador:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. O contêiner DIV deve ser adicionado ao &quot;titular&quot; DIV existente. O código a seguir é um exemplo completo de como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
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

A página de exemplos a seguir ilustra mais o uso real de incorporação de design responsivo com altura irrestrita:

[Demonstrações em tempo real](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporação responsiva de design com largura e altura definidas**

Se houver incorporação de design responsivo com largura e altura definidas, o estilo da página da Web será diferente; ele fornecerá ambos os tamanhos para o &quot; titular&quot; `DIV` e centralizá-lo na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` como 100%:

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

O restante das etapas de incorporação são idênticas à incorporação responsiva com altura irrestrita. O exemplo resultante é

```html {.line-numbers}
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

**Incorporando usando API baseada em Setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. Com essa API, o construtor não aceita parâmetros e os parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir ilustra a incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
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
