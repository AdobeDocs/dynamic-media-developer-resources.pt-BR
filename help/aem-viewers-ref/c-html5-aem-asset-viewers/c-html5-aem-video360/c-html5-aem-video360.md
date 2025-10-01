---
title: Video360
description: O HTML5 Video360 Viewer é um player de vídeo de 360 graus que reproduz streaming e vídeo progressivo 360 codificado no formato H.264, fornecido pela Dynamic Media Classic ou pela Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 2d4a26d04e11f544b4cbabaca592d77cfa2241d3
workflow-type: tm+mt
source-wordcount: '2179'
ht-degree: 0%

---

# Video360{#video}

O HTML5 Video360 Viewer é um player de vídeo de 360 graus que reproduz streaming e vídeo progressivo 360 codificado no formato H.264, fornecido pela Dynamic Media Classic ou pela Adobe Experience Manager, Dynamic Media.

Vídeos de 360 graus, também conhecidos como vídeos imersivos ou vídeos esféricos, são gravações de vídeo em que uma visualização em todas as direções é gravada ao mesmo tempo, filmada usando uma câmera omnidirecional ou uma coleção de câmeras. Há suporte para vídeo único e Conjuntos de vídeos adaptados. O visualizador também é compatível com o trabalho com fluxos de vídeo progressivo e HLS hospedados em um local externo.

A taxa de proporção recomendada para vídeo 360 é 2:1. Não há suporte para som espacial. O visualizador foi projetado para funcionar somente com vídeo 360; uma tentativa de reproduzir um vídeo não-360 resulta em uma reprodução de vídeo distorcida.

O visualizador foi projetado para funcionar em navegadores da Web móveis e de desktop compatíveis com vídeo HTML5. O visualizador é compatível com ferramentas opcionais de compartilhamento em redes sociais.

O Visualizador de vídeo 360 usa a reprodução de vídeo de transmissão HTML5 no formato HLS em sua configuração padrão sempre que o sistema subjacente suporta isso. Em sistemas que não suportam transmissão contínua do HTML5, o visualizador retorna à entrega de vídeo progressiva do HTML5.

Tipo de visualizador 517.

<!--
## Demo URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

-->

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador do HTML5 Video360 representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do HTML5 Viewer SDK usados por esse visualizador, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Visualizador do HTML5 Video360 pode ser usado no modo pop-up usando a página do HTML pronta para produção fornecida com os Visualizadores IS ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e a atribuição de capa são semelhantes às dos outros visualizadores descritos neste guia. Toda a atribuição de capa é obtida por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

O conteúdo de vídeo 360 requer configurações de codificação mais altas do que o vídeo não-360 padrão. Em outras palavras, o conteúdo 360 deve vir em resolução maior do que o vídeo não-360 para alcançar a mesma qualidade perceptível. É recomendável considerar as seguintes configurações de Predefinição de vídeo adaptável para vídeos 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Observe, no entanto, que veicular vídeos codificados com essas configurações de alta qualidade requer uma conexão de alta largura de banda no dispositivo de um usuário final.

## Interação com o visualizador de Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador do HTML5 Video360 fornece um conjunto de controles padrão de interface do usuário para reprodução de vídeo, como o botão reproduzir/pausar, a bolha de tempo de vídeo do depurador de vídeo, o indicador de tempo/tempo total reproduzido, o controle de volume e o botão de tela cheia. Todos esses controles estão agrupados na barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador também é compatível com várias ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário do, que se expande para uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido a restrições de segurança do navegador da Web.

O visualizador suporta a reprodução de vídeo 360 no seguinte:

* Headsets VR (como Oculus Go e Oculus Rift)
* Montagens VR HMD (montados na cabeça) (como Google Cardboard)
* Dispositivos não habilitados para VR (como navegadores de desktop, tablets e celulares não conectados a montagens VR HMD)

Nenhuma configuração adicional é necessária para visualizar o conteúdo de vídeo 360 no headset VR. O visualizador detecta automaticamente a presença do headset VR e mostra o botão &quot;VR&quot; sobre o conteúdo de vídeo. A ativação desse botão &quot;VR&quot; alterna a renderização de vídeo para o modo VR. O visualizador é compatível com a renderização VR somente em navegadores com suporte a WebVR.

Para usar montagens VR HMD, o modificador `Video360Player.vrrender` deve ser definido como `1` na configuração do visualizador, o que força a renderização estereoscópica.

Nos auscultadores VR e montagens VR HMD, a mudança de ponto de vista acontece em resposta ao movimento do auscultador, não é fornecido outro controle de reprodução no modo VR.

Ao assistir a 360 vídeos em dispositivos que não tenham VR habilitado, o usuário final pode usar mouse, toque ou teclado para controlar a reprodução e o ponto de vista do vídeo.

O visualizador é compatível com entrada por toque e entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

O visualizador é totalmente acessível pelo teclado. Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Normalmente, somente um vídeo pode ser reproduzido de cada vez. Quando um usuário começa a reproduzir um vídeo e, em seguida, tenta reproduzir outro vídeo, o primeiro vídeo é pausado automaticamente. O vídeo que foi pausado automaticamente lembra seu tempo de reprodução atual, para que o usuário possa sempre voltar e retomar a reprodução. A única exceção para essa regra é o navegador Chrome em dispositivos Android™ 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada do JavaScript `window.open()`, o elemento do HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página de HTML predefinida para o modo de operação pop-up. Ele é chamado de [!DNL Video360Viewer.html] e está localizado na subpasta [!DNL html5/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

<!--
The following is an example of HTML code that opens the viewer in a new window:
-->

<!--
```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```
-->

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
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho do HTML. Antes de usar a API do visualizador, inclua [!DNL Video360Viewer.js]. O arquivo [!DNL Video360Viewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

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
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7video360viewer` em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado, que será posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - Por demanda ou passado explicitamente usando o comando `style`.

   Consulte [Personalizando o visualizador de Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página do HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   É possível definir o modificador `stagesize` no registro de predefinição do visualizador no AEM Assets - por demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de Comandos, desta forma:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.Video360Viewer`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner do visualizador e o objeto JSON `params` aninhado com parâmetros de configuração com suporte do visualizador.

   Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl`, e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código, URL do servidor de vídeo transmitida como propriedade `videoserverurl`, ativo inicial como parâmetro `asset` e dados interativos como propriedade `interactivedata`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando isso acontece, o carregamento do visualizador é retomado automaticamente.

<!--
   The following is an example of creating a viewer instance, passing the minimum necessary configuration options to the constructor and calling the `init()` method. The example assumes the following:

    * The viewer instance is `video360Viewer`. 
    * The name of placeholder `DIV` is `s7viewer`. 
    * The Image Serving URL is `https://s7d9.scene7.com/is/image`. 
    * The video server URL is `https://s7d9.scene7.com/is/content`. 
    * The asset is `Viewers/space_station_360-AVS`.
-->

<!--

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

-->

<!--
   The following code is a complete example of a trivial web page that embeds the Video360 Viewer with a fixed size:
-->

<!--
   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
 ```
 -->

<!--  
**Responsive design embedding with unrestricted height**

With responsive design embedding, the web page normally has some kind of flexible layout in place that dictates the runtime size of the viewer's container `DIV`. For the following example, assume that the web page allows the viewer's container `DIV` to take 40% of the web browser window size, leaving its height unrestricted. The web page HTML code would look like the following:
-->

<!--
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
-->

<!--
Adding the viewer to such a page is similar to the steps for fixed size embedding. The only difference is that you do not need to explicitly define the viewer size.

1. Adding the viewer JavaScript file to your web page. 
1. Defining the container DIV. 
1. Creating and initializing the viewer.

All the steps above are the same as with the fixed size embedding. Add the container DIV to the existing `"holder"` DIV. 

The following code is a complete example. Notice how viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.
-->

<!--
```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```
-->

<!--
**Responsive Embedding with Width and Height Defined**

If there is responsive embedding with width and height defined, the web page styling is different. It provides both sizes to the `"holder"` DIV and center it in the browser window. Also, the web page sets the size of the `HTML` and `BODY` element to 100 percent.
-->

<!--
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
-->

<!--
The rest of the embedding steps are identical to the steps used for responsive embedding with unrestricted height. 

The resulting example is the following:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

-->


<!--
**Embedding Using Setter-based API**

Instead of using JSON-based initialization, it is possible to use setter-based API and no-args constructor. Using this API constructor does not take any parameters and configuration parameters are specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

The following example illustrates using fixed size embedding with the setter-based API:

-->

<!--

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```

-->

