---
title: Video360
description: O visualizador HTML5 Video360 é um player de vídeo de 360 graus que reproduz streaming e vídeo progressivo 360 codificado no formato H.264, fornecido pela Dynamic Media Classic ou pela Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Video360{#video}

O visualizador HTML5 Video360 é um player de vídeo de 360 graus que reproduz streaming e vídeo progressivo 360 codificado no formato H.264, fornecido pela Dynamic Media Classic ou pela Adobe Experience Manager, Dynamic Media.

Vídeos de 360 graus, também conhecidos como vídeos imersivos ou vídeos esféricos, são gravações de vídeo em que uma visualização em todas as direções é gravada ao mesmo tempo, filmada usando uma câmera omnidirecional ou uma coleção de câmeras. Há suporte para vídeo único e Conjuntos de vídeos adaptados. O visualizador também suporta o trabalho com vídeo progressivo e fluxos HLS hospedados em um local externo.

A taxa de proporção recomendada para vídeos 360 é 2:1. Não há suporte para som espacial. O visualizador foi projetado para funcionar somente com vídeo 360; uma tentativa de reproduzir um vídeo não-360 resulta em uma reprodução de vídeo distorcida.

O visualizador foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. O visualizador é compatível com ferramentas opcionais de compartilhamento em redes sociais.

O Video360 Viewer usa a reprodução de vídeo de streaming HTML5 no formato HLS em sua configuração padrão sempre que o sistema subjacente suportar isso. Em sistemas que não suportam transmissão contínua de HTML5, o visualizador retorna à entrega de vídeo progressiva de HTML5.

Tipo de visualizador 517.

## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador HTML5 Video360 representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do SDK do Visualizador HTML5 usados por esse visualizador, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Visualizador HTML5 Video360 pode ser usado no modo pop-up usando a página de HTML pronta para produção fornecida com os Visualizadores IS ou no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e a atribuição de capa são semelhantes às dos outros visualizadores descritos neste guia. Toda a atribuição de capa é obtida por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

O conteúdo de vídeo 360 requer configurações de codificação mais altas do que o vídeo não-360 padrão. Em outras palavras, o conteúdo 360 deve vir em resolução maior do que o vídeo não-360 para alcançar a mesma qualidade perceptível. É recomendável considerar as seguintes configurações de Predefinição de vídeo adaptável para vídeos 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Observe, no entanto, que veicular vídeos codificados com essas configurações de alta qualidade requer uma conexão de alta largura de banda no dispositivo de um usuário final.

## Interação com o visualizador de Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

O Visualizador do HTML5 Video360 fornece um conjunto de controles padrão de interface do usuário para reprodução de vídeo, como o botão reproduzir/pausar, bolhas de tempo de vídeo do depurador de vídeo, indicador de tempo/tempo total reproduzido, controle de volume e botão de tela cheia. Todos esses controles estão agrupados na barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador também é compatível com várias ferramentas de compartilhamento de redes sociais. Eles estão disponíveis como um único botão na interface do usuário do, que se expande para uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido a restrições de segurança do navegador da Web.

O visualizador suporta a reprodução de vídeo 360 no seguinte:

* Headsets VR (como Oculus Go e Oculus Rift)
* Montagens VR HMD (montados na cabeça) (como Google Cardboard)
* Dispositivos não habilitados para VR (como navegadores de desktop, tablets e celulares não conectados a montagens VR HMD)

Nenhuma configuração adicional é necessária para visualizar o conteúdo de vídeo 360 no headset VR. O visualizador detecta automaticamente a presença do headset VR e mostra o botão &quot;VR&quot; sobre o conteúdo de vídeo. A ativação desse botão &quot;VR&quot; alterna a renderização de vídeo para o modo VR. O visualizador é compatível com a renderização VR somente em navegadores com suporte a WebVR.

Para utilizar montagens VR HMD, o `Video360Player.vrrender` o modificador deve ser definido como `1` na configuração do visualizador, que força a renderização estereoscópica.

Nos auscultadores VR e montagens VR HMD, a mudança de ponto de vista acontece em resposta ao movimento do auscultador, não é fornecido outro controle de reprodução no modo VR.

Ao assistir a 360 vídeos em dispositivos que não tenham VR habilitado, o usuário final pode usar mouse, toque ou teclado para controlar a reprodução e o ponto de vista do vídeo.

O visualizador é compatível com entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse, no entanto, esse suporte é limitado apenas ao Chrome, Internet Explorer 11 e navegadores da Web Edge.

O visualizador é totalmente acessível pelo teclado. Consulte [Acessibilidade e navegação pelo teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela do navegador separada. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela do navegador. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsiva.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Normalmente, somente um vídeo pode ser reproduzido de cada vez. Quando um usuário começa a reproduzir um vídeo e, em seguida, tenta reproduzir outro vídeo, o primeiro vídeo é pausado automaticamente. O vídeo que foi pausado automaticamente lembra seu tempo de reprodução atual, para que o usuário possa sempre voltar e retomar a reprodução. A única exceção dessa regra é o navegador Chrome em dispositivos Android™ 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Ela ocupa toda a área da janela do navegador e é ajustada caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` Chamada de JavaScript, configurada corretamente `A` elemento HTML ou qualquer outro método adequado.

É recomendável usar uma página de HTML para o modo de operação pop-up. É chamado de [!DNL Video360Viewer.html] e está localizado sob o [!DNL html5/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Veja a seguir um exemplo do código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio imobiliário de uma página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva de design presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura irrestrita, o visualizador escolhe automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de design da Web, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preenche apenas essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do contêiner `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua [!DNL Video360Viewer.js]. A variável [!DNL Video360Viewer.js] O arquivo está localizado sob o [!DNL html5/js/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Fazer referência apenas ao JavaScript do visualizador principal `include` arquivo na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Em particular, não faça referência direta ao SDK do HTML5 `Utils.js` biblioteca carregada pelo visualizador de `/s7viewers` caminho de contexto (o chamado SDK consolidado) `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução são totalmente gerenciadas pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, ao inserir uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do contêiner `DIV`.

   Adicionar um vazio `DIV` elemento para a página onde deseja que o visualizador apareça. A variável `DIV` O elemento deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio de CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a variável `position` A propriedade CSS está definida como `relative` ou `absolute`.

   Para que o recurso de tela cheia funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM com uma ordem de empilhamento superior à do espaço reservado `DIV`.

   Veja a seguir um exemplo de um espaço reservado definido `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7video360viewer` classe CSS de nível superior em unidades absolutas ou usando `stagesize` modificador.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado, que será posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - On-demand ou passado explicitamente usando `style` comando.

   Consulte [Personalização do visualizador do Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Você pode definir a variável `stagesize` modificador no registro de predefinição do visualizador no AEM Assets - sob demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com `params` ou como uma chamada de API conforme descrito na seção Referência de comandos, desta forma:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância de `s7viewers.Video360Viewer` classe, transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter `containerId` campo que contém o nome da ID do contêiner de visualização e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador.

   Neste caso, o `params` objeto deve ter pelo menos o URL do Servidor de imagens passado como `serverUrl` propriedade e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código, URL do servidor de vídeo transmitido como `videoserverurl` propriedade, ativo inicial como `asset` e dados interativos como `interactivedata` propriedade. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o `init()` método antes do fechamento `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, pode ser oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando isso acontece, o carregamento do visualizador é retomado automaticamente.

   Veja a seguir um exemplo de criação de uma instância do visualizador, passando as opções de configuração mínimas necessárias para o construtor e chamando o `init()` método. O exemplo assume o seguinte:

   * A instância do visualizador é `video360Viewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * O URL do servidor de imagens é `https://s7d9.scene7.com/is/image`.
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

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o visualizador Video360 com um tamanho fixo:

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

**Incorporação responsiva de design com altura irrestrita**

Com a incorporação responsiva de design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do container do visualizador `DIV`. Para o exemplo a seguir, considere que a página da Web permite o container do visualizador `DIV` para obter 40% do tamanho da janela do navegador web, deixando sua altura irrestrita. O código de HTML da página da Web seria semelhante ao seguinte:

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

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do container DIV.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicionar o contêiner DIV ao existente `"holder"` DIV O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

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

**Incorporação responsiva com Largura e Altura definidas**

Se houver incorporação responsiva com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centralize-o na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%.

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

**Incorporação usando API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`, e `setAsset()` Métodos de API do com chamadas de JavaScript separadas.

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
