---
title: Vídeo360
description: O visualizador HTML5 Video360 é um player de vídeo de 360 graus que reproduz streaming e vídeo 360 progressivo codificado no formato H.264, fornecido pelo Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Vídeo360{#video}

O visualizador HTML5 Video360 é um player de vídeo de 360 graus que reproduz streaming e vídeo 360 progressivo codificado no formato H.264, fornecido pelo Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.

Vídeos de 360 graus, também conhecidos como vídeos imersivos ou esféricos, são gravações de vídeo em que uma exibição em todas as direções é gravada ao mesmo tempo, fotografada com uma câmera onidirecional ou uma coleção de câmeras. Vídeo único e Conjuntos de vídeo adaptativo são suportados. O visualizador também oferece suporte para trabalhar com vídeos progressivos e fluxos HLS hospedados em um local externo.

A taxa de proporção recomendada para o vídeo 360 é de 2:1. Não há suporte para som espacial. O visualizador foi projetado para funcionar somente com vídeo 360; uma tentativa de reproduzir um vídeo que não seja 360 resulta na reprodução distorcida do vídeo.

O visualizador foi projetado para funcionar em navegadores para desktop e dispositivos móveis da Web que suportam vídeo HTML5. O visualizador aceita ferramentas opcionais de compartilhamento em redes sociais.

O visualizador Video360 usa a reprodução de vídeo de transmissão HTML5 no formato HLS em sua configuração padrão, sempre que o sistema subjacente suportar isso. Em sistemas que não suportam streaming de HTML5, o visualizador volta para a entrega de vídeo progressivo do HTML5.

O tipo de visualizador é 517.

## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador HTML5 usados por esse visualizador, ativos, CSS) baixados pelo visualizador no tempo de execução.

HTML5 Video360 Viewer pode ser usado em modo pop-up usando a página HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e o skinning são semelhantes aos dos outros visualizadores descritos neste guia. Todo o esfolamento é obtido por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

O conteúdo de vídeo 360 requer configurações de codificação mais altas do que o vídeo padrão não-360. Em outras palavras, o conteúdo de 360 deve ser exibido em resolução maior do que o vídeo de não 360, a fim de alcançar a mesma qualidade perceptível. É recomendável considerar as seguintes configurações de predefinição de vídeo adaptável para o vídeo 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Observe, no entanto, que veicular vídeos codificados com configurações de alta qualidade requer uma conexão de alta largura de banda no dispositivo de um usuário final.

## Interação com o visualizador Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer fornece um conjunto de controles padrão da interface do usuário para a reprodução do vídeo, como o botão reproduzir/pausar, a bolha de tempo do vídeo do depurador de vídeo, o indicador de tempo de reprodução/tempo total, o controle de volume e o botão de tela cheia. Todos esses controles são agrupados em barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador também é compatível com várias ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário, que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código de incorporação e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento de incorporação ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. O compartilhamento de ferramentas não está disponível no modo de tela cheia devido a restrições de segurança do navegador da Web.

O visualizador oferece suporte para a reprodução de vídeo 360 no seguinte:

* Cabeçalhos VR (como Oculus Go e Oculus Rift)
* Montagens VR HMD (monitor montado na cabeça) (como Google Cardboard)
* Dispositivos não habilitados para VR (como navegadores para desktop, tablets e telefones celulares não conectados a montagens VR HMD)

Nenhuma configuração adicional é necessária para exibir o conteúdo de vídeo 360 no fone de ouvido VR. O visualizador detecta automaticamente a presença de fone de ouvido VR e mostra o botão &quot;VR&quot; sobre o conteúdo de vídeo. A ativação desse botão &quot;VR&quot; altera a renderização do vídeo para o modo VR. O visualizador suporta renderização VR somente em navegadores com suporte para WebVR.

Para usar montagens VR HMD, a variável `Video360Player.vrrender` modificador deve ser definido como `1` na configuração do visualizador, que força a renderização estereoscópica.

Em fones de VR e montagens VR HMD, ocorre uma alteração de ponto de vista em resposta ao movimento do fone de ouvido, e nenhum outro controle de reprodução é fornecido no modo VR.

Ao assistir a vídeos 360 em dispositivos não habilitados para VR, o usuário final pode usar mouse, toque ou teclado para controlar a reprodução e o ponto de vista do vídeo.

O visualizador aceita entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

O visualizador é totalmente acessível por teclado. Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Como incorporar o visualizador Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Geralmente, apenas um vídeo pode ser reproduzido de cada vez. Quando um usuário começa a reproduzir um vídeo e tenta reproduzir outro, o primeiro é pausado automaticamente. O vídeo que foi pausado automaticamente lembra do tempo de reprodução atual, para que o usuário possa sempre retornar a ele e retomar a reprodução. A única exceção dessa regra é no navegador Chrome em dispositivos Android™ 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` Chamada de JavaScript, configurada corretamente `A` HTML ou qualquer outro método adequado.

É recomendável usar uma página de HTML pronta para uso no modo de operação pop-up. É chamado de [!DNL Video360Viewer.html] e está localizado sob a [!DNL html5/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas parte do imóvel de uma página da web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, além de páginas projetadas responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação de design responsivo supõe que o visualizador deve ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolhe automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de web design, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preenche apenas essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no HTML head. Antes de usar a API do visualizador, verifique se você incluiu [!DNL Video360Viewer.js]. O [!DNL Video360Viewer.js] O arquivo está localizado sob a variável [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores da Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores da Adobe Dynamic Media Classic que têm os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Referencie somente o JavaScript do visualizador principal `include` na sua página. Não faça referência a arquivos JavaScript adicionais no código da página da Web que possam ser baixados pela lógica do visualizador em tempo de execução. Em particular, não faça referência diretamente ao SDK do HTML5 `Utils.js` biblioteca carregada pelo visualizador de `/s7viewers` caminho do contexto (o chamado SDK consolidado) `include`). O motivo é que a localização da variável `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução são totalmente gerenciadas pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página, interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do contêiner `DIV`.

   Adicionar um vazio `DIV` para a página onde você deseja que o visualizador apareça. O `DIV` deve ter a ID definida, pois essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a variável `position` A propriedade CSS está definida como `relative` ou `absolute`.

   Para que o recurso de tela cheia funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento maior do que o espaço reservado `DIV`.

   Este é um exemplo de um espaço reservado definido `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7video360viewer` classe CSS de nível superior em unidades absolutas ou usando `stagesize` modificador.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - On-demand ou passado explicitamente usando `style` comando.

   Consulte [Personalização do visualizador de vídeo 360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre o estilo do visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   É possível definir a variável `stagesize` modificador no registro predefinido do visualizador no AEM Assets - sob demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com `params` ou como uma chamada de API conforme descrito na seção Referência de comando , desta forma:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.Video360Viewer` classe , transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter `containerId` campo que contém o nome da ID do contêiner do visualizador e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador.

   Nesse caso, a variável `params` O objeto deve ter pelo menos o URL de disponibilização de imagens passado como `serverUrl` e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código, URL do servidor de vídeo passado como `videoserverurl` propriedade, ativo inicial como `asset` e dados interativos como `interactivedata` propriedade. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame a função `init()` método antes de fechar `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, pode estar oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso acontece, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando a função `init()` método . O exemplo assume o seguinte:

   * A instância do visualizador é `video360Viewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * O URL de disponibilização de imagens é `https://s7d9.scene7.com/is/image`.
   * O URL do servidor de vídeo é `https://s7d9.scene7.com/is/content`.
   * O ativo é `Viewers/space_station_360-AVS`.

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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de vídeo360 com um tamanho fixo:

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

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação responsiva do design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho de tempo de execução do contêiner do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita o contêiner do visualizador `DIV` para obter 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código de HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o DIV do contêiner ao `"holder"` DIV. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

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

**Incorporação responsiva com definição de largura e altura**

Se houver incorporação responsiva com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para a variável `"holder"` DIV e centralize-o na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%.

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

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não utiliza parâmetros e parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`e `setAsset()` Métodos de API com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

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
