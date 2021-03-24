---
description: Visualizador de vídeo interativo é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.
solution: Experience Manager
title: Vídeo interativo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---


# Vídeo interativo{#interactive-video}

Visualizador de vídeo interativo é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.

O visualizador também mostra amostras interativas de produtos ao lado do conteúdo do vídeo. Vídeo único e Conjuntos de vídeo adaptativo são suportados. Ele foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. O visualizador aceita legendas ocultas opcionais exibidas sobre conteúdo de vídeo, navegação de capítulo de vídeo e ferramentas de compartilhamento social. O objetivo desse visualizador é ajudar você a implementar uma experiência de &quot;vídeo que pode ser comprado&quot;. Ou seja, os usuários podem selecionar uma amostra associada a uma região específica do tempo do vídeo e ser redirecionados para uma Exibição rápida ou para uma página de detalhes do produto no site do cliente.

O tipo de visualizador é 510.

## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

e

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Usando o Visualizador de Vídeo Interativo {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de vídeo interativo representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos e CSS) baixados pelo visualizador em tempo de execução.

O Visualizador de vídeo interativo pode ser usado no modo pop-up usando uma página HTML pronta para produção fornecida com os Visualizadores de exibição de imagem. Ele também pode ser usado no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e a definição são semelhantes às dos outros visualizadores descritos neste guia. Todo o esfolamento é obtido por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de vídeo interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador de vídeo interativo fornece um conjunto de controles padrão da interface do usuário para a reprodução do vídeo, como um botão Reproduzir/Pausar, depurador de vídeo, bolha de tempo do vídeo, indicador de tempo de reprodução/tempo total, controle de volume, botão de tela cheia e alternância de legenda fechada. Todos esses controles são agrupados em uma barra de controle diretamente na exibição principal.

Observe que, em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador mostra um painel com amostras interativas à direita da área de visualização de vídeo. A lista de amostras avança automaticamente à medida que o vídeo é reproduzido, de modo que as amostras correspondentes à região do vídeo atual sejam exibidas. Clicar ou tocar em uma amostra aciona uma ação que foi associada a essa amostra durante o tempo de criação. Dependendo de como você o configurou, o acionador pode redirecionar para uma página diferente no site ou transmitir informações do produto de volta à lógica da página da Web, que, por sua vez, pode acionar a abertura de uma Exibição rápida que mostra o conteúdo relacionado do produto.

É possível navegar pelo conteúdo do vídeo rapidamente quando a filtragem de vídeo é ativada. Os capítulos de vídeo são exibidos como marcadores no rastreamento do depurador de vídeo e mostram o título e a descrição do capítulo ao passar o mouse (ou em um único toque nos sistemas de toque). O cliente pode &quot;procurar&quot; um capítulo específico clicando em um marcador de capítulo ou tocando em uma bolha de descrição do capítulo.

O visualizador também aceita diversas ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário, que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código de incorporação e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento de incorporação ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. O compartilhamento de ferramentas não está disponível no modo de tela cheia devido a restrições de segurança do navegador da Web.

O visualizador é totalmente acessível por teclado. Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando visualizador de vídeo interativo {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de vídeo interativo foi projetado para ser incorporado à página de hospedagem. Essa página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para tamanhos de janela de navegador diferentes.

Para acomodar essas necessidades, o visualizador aceita dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas parte do imóvel de uma página da web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, além de páginas projetadas responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva de design supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de design da Web, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, inclua [!DNL InterativeVideoViewer.js]. O arquivo [!DNL InteractiveVideoViewer.js] está localizado na subpasta [!DNL html5/js/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic que tenham os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript `include` do visualizador principal na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador em tempo de execução. Em particular, não faça referência diretamente à biblioteca de SDK `Utils.js` HTML5 carregada pelo visualizador do `/s7viewers` caminho de contexto (o chamado SDK consolidado `include`). O motivo é que o local de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciado pela lógica do visualizador e o local muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão de produto for implantada.

1. Definindo o contêiner `DIV`.

   Adicione um elemento `DIV` vazio à página onde você deseja que o visualizador apareça. O elemento `DIV` deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Para que o recurso de tela cheia funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento mais alta do que seu espaço reservado `DIV`.

   A seguir, um exemplo de um elemento `DIV` de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7interactivevideoviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no AEM Assets - sob demanda ou passado explicitamente usando o comando `style`.

   Consulte [Personalizando visualizador de vídeo interativo](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro de predefinição do visualizador no AEM Assets - sob demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de comandos , desta forma:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Após concluir as etapas acima, crie uma instância de `s7viewers.InteractiveVideoViewer` classe, passe todas as informações de configuração para seu construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do contêiner do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador.

   Nesse caso, o objeto `params` deve ter pelo menos o URL de Exibição de Imagem passado como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código, URL do servidor de vídeo passado como propriedade `videoserverurl`, ativo inicial como parâmetro `asset` e dados interativos como propriedade `interactivedata`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame o método `init()` antes de fechar a tag `BODY` ou no evento body `onload()` .

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. O que acontece, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando o método `init()`. O exemplo assume o seguinte:

   * A instância do visualizador é `interactiveVideoViewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * O URL de disponibilização de imagens é `https://aodmarketingna.assetsadobe.com/is/image/`.
   * O URL do servidor de vídeo é `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * O URL de conteúdo é `https://aodmarketingna.assetsadobe.com/`.
   * O ativo é `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Os dados interativos são `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de Vídeo Interativo com um tamanho fixo:

   ```
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

**Incorporação de design responsivo com altura irrestrita**

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

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporação responsiva com definição de largura e altura**

No caso de incorporação responsiva com largura e altura definidas, o estilo da página da Web é diferente. Ela fornece ambos os tamanhos para o `"holder"` DIV e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%.

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

O restante das etapas de incorporação são idênticas às etapas usadas para incorporação responsiva com altura irrestrita. O exemplo resultante é o seguinte:

```
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

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não utiliza parâmetros e parâmetros de configuração são especificados usando `setContainerId()`, `setParam()` e `setAsset()` métodos de API com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

