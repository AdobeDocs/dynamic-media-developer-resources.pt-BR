---
description: O Interative Video Viewer é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.
seo-description: O Interative Video Viewer é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.
seo-title: Vídeo interativo
solution: Experience Manager
title: Vídeo interativo
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Vídeo interativo{#interactive-video}

O Interative Video Viewer é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264.

O visualizador do visualizador também mostra amostras interativas de produtos ao lado do conteúdo de vídeo. Vídeo único e Conjuntos de vídeo adaptáveis são suportados. Ele foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. O visualizador oferece suporte a legendas ocultas opcionais exibidas sobre o conteúdo de vídeo, navegação por capítulo de vídeo e ferramentas de compartilhamento em redes sociais. O objetivo deste visualizador é ajudá-lo a implementar uma experiência de &quot;vídeo que pode ser comprado&quot;. Ou seja, os usuários podem selecionar uma amostra associada a uma região específica de tempo de vídeo e ser redirecionados para uma Visualização rápida ou para uma página de detalhes do produto no site do cliente.

O tipo de visualizador é 510.

## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

e

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte Requisitos [do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do Visualizador de vídeo interativo {#section-e6c68406ecdc4de781df182bbd8088b4}

O Interative Video Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do Viewer SDK usados por esse visualizador específico, ativos e CSS) baixados pelo visualizador em tempo de execução.

O Visualizador de vídeo interativo pode ser usado no modo pop-up usando a página HTML pronta para produção fornecida com os Visualizadores do Servidor de imagens. Ele também pode ser usado no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e a capa são semelhantes às dos outros visualizadores descritos neste guia. Toda a esfola é alcançada por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte Referência de [comando comum a todos os visualizadores - Referência de atributos](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuração e [comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador de vídeo interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Interative Video Viewer fornece um conjunto de controles padrão da interface do usuário para reprodução de vídeo, como um botão Reproduzir/Pausar, depurador de vídeo, bolha de tempo de vídeo, indicador de tempo de reprodução/tempo total, controle de volume, botão de tela cheia e alternância de legenda fechada. Todos esses controles são agrupados em uma barra de controle logo abaixo da visualização principal.

Observe que em dispositivos de toque o controle de volume fica oculto da interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador mostra um painel com amostras interativas à direita da área de visualização de vídeo. A lista de amostras avança automaticamente à medida que o vídeo é reproduzido, para que as amostras correspondentes à região do vídeo atual sejam exibidas. Clicar ou tocar em uma amostra aciona uma ação que foi associada a essa amostra durante o tempo do autor. Dependendo de como você o configurou, o acionador pode redirecionar para uma página diferente no site ou retornar as informações do produto à lógica da página da Web, o que, por sua vez, pode acionar a abertura de uma Visualização Rápida que mostra o conteúdo do produto relacionado.

É possível navegar pelo conteúdo do vídeo rapidamente quando a captação do vídeo é ativada. Os capítulos de vídeo são exibidos como marcadores na faixa do depurador de vídeo e mostram o título e a descrição do capítulo ao passar o mouse (ou em um único toque nos sistemas de toque). O cliente pode &quot;buscar&quot; para um capítulo específico clicando em um marcador de capítulo ou tocando em uma bolha de descrição do capítulo.

O visualizador também suporta diversas ferramentas de compartilhamento de mídia social. Eles estão disponíveis como um único botão na interface do usuário que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento suportado, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido às restrições de segurança do navegador da Web.

O visualizador está totalmente acessível pelo teclado. Consulte [Acessibilidade e navegação](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)do teclado.

## Como incorporar o Visualizador de vídeo interativo {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de vídeo interativo foi projetado para ser incorporado à página de hospedagem. Tal página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes.

Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio de uma página da web.

Os casos de uso principal são páginas da Web orientadas para desktops ou tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web que têm um layout estático.

A incorporação responsiva do design supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração do tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à visualização, sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas de web design, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho que o layout da página da Web fornece. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de poder usar a API do visualizador, verifique se você incluiu [!DNL InterativeVideoViewer.js]. O [!DNL InteractiveVideoViewer.js] arquivo está localizado na [!DNL html5/js/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal na sua página. `include` Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à `Utils.js` biblioteca do SDK HTML5 carregada pelo visualizador a partir do caminho de `/s7viewers` contexto (o chamado SDK consolidado `include`). O motivo é que a localização das bibliotecas do visualizador do tempo de execução `Utils.js` ou semelhantes é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. A Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definição do container `DIV`.

   Adicione um `DIV` elemento vazio à página onde deseja que o visualizador apareça. O `DIV` elemento deve ter sua ID definida, pois ela é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   Para que o recurso de tela cheia funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento superior à do espaço reservado `DIV`.

   A seguir está um exemplo de um elemento de espaço reservado definido `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático para o visualizador declarando-o para a classe CSS de nível `.s7interactivevideoviewer` superior em unidades absolutas ou usando o `stagesize` modificador.

   Você pode colocar o dimensionamento no CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador nos ativos AEM - sob demanda ou transmitido explicitamente usando o `style` comando.

   Consulte [Personalização do visualizador](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de vídeo interativo para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Você pode definir o `stagesize` modificador no registro predefinido do visualizador nos ativos AEM - sob demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com `params` coleção ou como uma chamada de API conforme descrito na seção Referência de comando, como:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.InteractiveVideoViewer` classe, passe todas as informações de configuração para seu construtor e chame o `init()` método em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter um `containerId` `params` campo que contém o nome da ID do container do visualizador e o objeto JSON aninhado com parâmetros de configuração suportados pelo visualizador.

   Nesse caso, o `params` objeto deve ter pelo menos o URL de disponibilização de imagem passado como `serverUrl` propriedade e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e start o visualizador com uma única linha de código, URL do servidor de vídeo passado como `videoserverurl` propriedade, ativo inicial como `asset` parâmetro e dados interativos como `interactivedata` propriedade. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o `init()` método imediatamente antes da `BODY` tag de fechamento ou no `onload()` evento body.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. O que acontece é que a carga do visualizador é retomada automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o `init()` método. O exemplo considera o seguinte:

   * A instância do visualizador é `interactiveVideoViewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * O URL de disponibilização de imagem é `https://aodmarketingna.assetsadobe.com/is/image/`.
   * O URL do servidor de vídeo é `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * O URL do conteúdo é `https://aodmarketingna.assetsadobe.com/`.
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de vídeo interativo com um tamanho fixo:

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

Adicionar o visualizador a uma página assim é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o DIV do container.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o DIV do container ao DIV existente. `"holder"` O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

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

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Incorporação responsiva com definição de largura e altura**

No caso de incorporação responsiva com largura e altura definidas, o estilo da página da Web é diferente. Fornece ambos os tamanhos para o `"holder"` DIV e centraliza-o na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%.

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

O restante das etapas de incorporação são idênticos às etapas usadas para incorporação responsiva com altura irrestrita. O exemplo resultante é o seguinte:

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

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando métodos `setContainerId()`, `setParam()`e `setAsset()` API com chamadas JavaScript separadas.

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

