---
title: Vídeo
description: O Visualizador de vídeo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pela Dynamic Media Classic ou Adobe Experience Manager com Dynamic Media.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Vídeo{#video}

O Visualizador de vídeo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pela Dynamic Media Classic ou Experience Manager com Dynamic Media.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Há suporte para vídeo único e Conjuntos de vídeos adaptados. Além disso, o visualizador suporta o trabalho com fluxos de vídeo progressivo e HLS hospedados em locais externos. Ele foi projetado para funcionar em navegadores da Web móveis e de desktop compatíveis com vídeo HTML5. Esse visualizador também oferece suporte a legendas ocultas opcionais que são exibidas sobre conteúdo de vídeo, navegação de capítulo de vídeo e ferramentas de compartilhamento de redes sociais.

O Visualizador de vídeo usa a reprodução de vídeo de transmissão HTML5 no formato HLS em sua configuração padrão, sempre que o sistema subjacente a suporta. Em sistemas que não suportam transmissão contínua do HTML5, o visualizador retorna à entrega de vídeo progressiva do HTML5.

Visualizador tipo 506.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Uso do visualizador de vídeo {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de vídeo representa um arquivo principal do JavaScript e um conjunto de arquivos auxiliares - um único JavaScript inclui todos os componentes do Viewer SDK usados por esse visualizador específico, ativos e CSS baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de vídeo no modo pop-up usando a página do HTML pronta para produção fornecida com os Visualizadores IS. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado em uma página da Web de destino usando a API documentada.

A tarefa de configurar e definir a aparência do visualizador é semelhante a outros visualizadores. Toda a atribuição de capa é obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o visualizador de vídeo {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de vídeo fornece um conjunto de controles padrão da interface do usuário para reprodução de vídeo, como um botão reproduzir/pausar, bolha de tempo de vídeo do depurador de vídeo, indicador de tempo/tempo total reproduzido, controle de volume, botão de tela cheia e botão de legenda oculta. Todos esses controles estão agrupados em uma barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões do hardware.

Quando o visualizador opera no modo pop-up, o botão de tela cheia não está disponível na interface do usuário.

É possível navegar pelo conteúdo de um vídeo rapidamente quando um capítulo de vídeo é ativado. Os capítulos de vídeo são exibidos como marcadores no rastreamento do depurador de vídeo e mostram o título do capítulo e a descrição associada em uma rolagem do mouse ou com um único toque em sistemas de toque. Os usuários podem buscar um capítulo específico selecionando um marcador de capítulo ou a bolha de descrição do capítulo.

O visualizador é compatível com entrada por toque e entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Ferramentas de compartilhamento de redes sociais com o Visualizador de vídeo {#section-907d316fe1da4b87abb9775f02464704}

O Visualizador de vídeo suporta ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário do, que se expande para uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela.

A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente.

As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido a restrições de segurança do navegador da Web.

## Incorporação do visualizador de vídeo {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Normalmente, somente um vídeo pode ser reproduzido de cada vez. Quando um usuário começa a reproduzir um vídeo e, em seguida, tenta reproduzir outro vídeo, o primeiro vídeo é pausado automaticamente. O vídeo que foi pausado automaticamente lembra seu tempo de reprodução atual, para que o usuário possa sempre voltar e retomar a reprodução. A única exceção para essa regra é o navegador Chrome em dispositivos Android™ 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento do HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página de HTML predefinida para o modo de operação pop-up. Ele é chamado de [!DNL VideoViewer.html] e está localizado na subpasta [!DNL html5/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Veja a seguir um exemplo do código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do espaço imobiliário da página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablet e também páginas de design responsivas que ajustam o layout automaticamente, dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor para páginas da Web com layout de página estático.

A incorporação de design responsivo presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar o visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Esse método garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam uma estrutura de layout de design responsiva, como Bootstrap ou Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho do HTML. Antes de usar a API do visualizador, inclua [!DNL FlyoutViewer.js]. O arquivo [!DNL FlyoutViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
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

   Verifique se o recurso de tela cheia funciona corretamente no Internet Explorer. Verifique se não há outros elementos no DOM com uma ordem de empilhamento superior à do espaço reservado DIV.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7videoviewer` em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado. Posteriormente, ele é atribuído a um registro de predefinição do visualizador no Dynamic Media Classic ou transmitido explicitamente usando um comando de estilo.

   Consulte [Personalizando o visualizador de vídeo](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obter mais informações sobre como estilizar o visualizador usando CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático em uma página do HTML:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro de predefinição do visualizador no Dynamic Media Classic, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params`. Ou, como uma chamada de API, conforme descrito na seção Referência de comandos, como no seguinte:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.VideoViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner de visualizador e o objeto JSON `params` aninhado com parâmetros de configuração com suporte do visualizador. Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens transmitida como propriedade `serverUrl`, a URL do servidor de vídeo transmitida como propriedade `videoserverurl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. Este exemplo supõe que `videoViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é a URL do Servidor de Imagens, [!DNL http://s7d1.scene7.com/is/content/] é a URL do servidor de vídeo e [!DNL Scene7SharedAssets/Glacier_Climber_MP4] é o ativo.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de vídeo com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporação responsiva de design com altura irrestrita**

Com a incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para fins deste exemplo, considere que a página da Web permite que o contêiner do visualizador `DIV` ocupe 40% do tamanho da janela do navegador da Web, deixando sua altura irrestrita. O código HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante à incorporação de tamanho fixo; a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicionar contêiner `DIV` ao &quot; titular&quot; existente `DIV`. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

A página de exemplos a seguir ilustra mais o uso real de incorporação de design responsivo com altura irrestrita:

[Demonstrações em tempo real](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=pt-BR)

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

As etapas de incorporação restantes são idênticas à incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
