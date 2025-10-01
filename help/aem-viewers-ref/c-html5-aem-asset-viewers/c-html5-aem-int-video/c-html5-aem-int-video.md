---
title: Vídeo interativo
description: O Visualizador de vídeo interativo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2177'
ht-degree: 0%

---

# Vídeo interativo{#interactive-video}

O Visualizador de vídeo interativo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.

O visualizador também mostra amostras de produtos interativas ao lado do conteúdo do vídeo. Há suporte para vídeo único e Conjuntos de vídeos adaptados. Ele foi projetado para funcionar em navegadores da Web móveis e de desktop compatíveis com vídeo HTML5. O visualizador é compatível com legendas ocultas opcionais exibidas sobre conteúdo de vídeo, navegação de capítulo de vídeo e ferramentas de compartilhamento em redes sociais. O objetivo desse visualizador é ajudá-lo a implementar uma experiência de &quot;vídeo que pode ser comprado&quot;. Ou seja, os usuários podem selecionar uma amostra associada a uma região de tempo de vídeo específica e ser redirecionados para uma página de detalhes do produto ou de Quickview no site do cliente.

Tipo de visualizador 510.


## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--
[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)
-->

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador de vídeo interativo {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de vídeo interativo representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares baixados pelo visualizador em tempo de execução. Uma única JavaScript é incluída com todos os componentes do Viewer SDK usados por esse visualizador, ativos e CSS específicos.

O Visualizador de vídeo interativo pode ser usado no modo pop-up usando a página do HTML pronta para produção fornecida com os Visualizadores do servidor de imagens. Ele também pode ser usado no modo incorporado, em que é integrado à página da Web direcionada usando a API documentada.

A configuração e a atribuição de capa são semelhantes às dos outros visualizadores descritos neste guia. Toda a atribuição de capa é obtida por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de vídeo interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador de vídeo interativo fornece um conjunto de controles padrão da interface do usuário para reprodução de vídeo, como um botão Reproduzir/Pausar, depurador de vídeo, bolha de tempo do vídeo, indicador de tempo/tempo total reproduzido, controle de volume, botão de tela cheia e botão de legenda oculta. Todos esses controles estão agrupados em uma barra de controle diretamente na exibição principal.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador mostra um painel com amostras interativas à direita da área de visualização do vídeo. A lista de amostras avança automaticamente à medida que o vídeo é reproduzido, para que as amostras correspondentes à região de vídeo atual sejam exibidas. Clicar ou tocar em uma amostra aciona uma ação que foi associada a essa amostra durante o tempo de criação. Dependendo de como você o configurou, o acionador pode redirecionar para uma página diferente no site. Ou ele pode enviar as informações do produto de volta à lógica da página da Web, o que, por sua vez, pode acionar a abertura de uma visualização rápida que mostra o conteúdo do produto relacionado.

É possível navegar pelo conteúdo do vídeo rapidamente quando um capítulo de vídeo é ativado. Os capítulos de vídeo são exibidos como marcadores no rastreamento do depurador de vídeo e mostram o título e a descrição do capítulo ao rolar (ou em um único toque em sistemas de toque). O cliente pode &quot;buscar&quot; um capítulo específico clicando em um marcador de capítulo ou tocando em uma bolha de descrição de capítulo.

O visualizador também é compatível com várias ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário do, que se expande para uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido a restrições de segurança do navegador da Web.

O visualizador é totalmente acessível pelo teclado. Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de vídeo interativo {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de vídeo interativo é incorporado à página de hospedagem. Essa página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela de navegador.

Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio imobiliário de uma página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa funcionalidade é a melhor opção para páginas da Web com layout estático.

A incorporação de design responsivo presume que o visualizador precisa redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de design da Web, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho do HTML. Antes de usar a API do visualizador, inclua [!DNL InterativeVideoViewer.js]. O arquivo [!DNL InteractiveVideoViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do HTML5 SDK carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, a inserção de uma referência direta a qualquer JavaScript `include` secundário usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definindo o container `DIV`.

   Adicione um elemento `DIV` vazio à página em que você deseja que o visualizador apareça. O elemento `DIV` deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio de CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Para que o recurso de tela inteira funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM com uma ordem de empilhamento maior do que a do espaço reservado `DIV`.

   Este é um exemplo de um elemento de espaço reservado `DIV` definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7interactivevideoviewer` em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento em CSS diretamente na página do HTML. Ou você pode colocá-lo em um arquivo CSS personalizado do visualizador, que será posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - Sob demanda ou passado explicitamente usando o comando `style`.

   Consulte [Personalizando o visualizador de vídeo interativo](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página do HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   É possível definir o modificador `stagesize` no registro de predefinição do visualizador em Experience Manager Assets - Por demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de Comandos, desta forma:

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.InteractiveVideoViewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner do visualizador e o objeto JSON `params` aninhado com parâmetros de configuração com suporte do visualizador.

   Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl`, e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código, URL do servidor de vídeo transmitida como propriedade `videoserverurl`, ativo inicial como parâmetro `asset` e dados interativos como propriedade `interactivedata`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner ainda não faz parte necessariamente do layout da página da Web. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Isso acontece; o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando as opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. O exemplo assume o seguinte:

   * A instância do visualizador é `interactiveVideoViewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * A URL do Servidor de Imagens é `https://aodmarketingna.assetsadobe.com/is/image/`.
   * A URL do servidor de vídeo é `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * A URL do conteúdo é `https://aodmarketingna.assetsadobe.com/`.
   * O ativo é `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Os dados interativos são `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de vídeo interativo com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações em tempo real](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporação responsiva com Largura e Altura definidas**

Se houver incorporação responsiva com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centralizá-lo na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` como 100%.

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
