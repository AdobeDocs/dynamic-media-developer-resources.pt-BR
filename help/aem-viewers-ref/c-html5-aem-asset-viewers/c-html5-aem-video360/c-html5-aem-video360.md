---
description: O HTML5 Video360 Viewer é um player de vídeo de 360 graus que reproduz streaming e vídeo 360 progressivo codificado no formato H.264, fornecido do Dynamic Media Classic ou AEM Dynamic Media.
solution: Experience Manager
title: Vídeo360
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '2582'
ht-degree: 0%

---


# Video360{#video}

O HTML5 Video360 Viewer é um player de vídeo de 360 graus que reproduz streaming e vídeo 360 progressivo codificado no formato H.264, fornecido do Dynmaic Media Classic ou da AEM Dynamic Media.

Vídeos de 360 graus, também conhecidos como vídeos imersivos ou esféricos, são gravações de vídeo em que uma visualização em todas as direções é gravada ao mesmo tempo, fotografada com uma câmera onidirecional ou uma coleção de câmeras. Vídeo único e Conjuntos de vídeo adaptáveis são suportados. O visualizador também suporta o trabalho com vídeo progressivo e fluxos HLS hospedados em um local externo.

A proporção recomendada para o vídeo 360 é 2:1. O som espacial não é suportado. O visualizador foi projetado para funcionar apenas com vídeo 360; uma tentativa de reproduzir um vídeo que não seja 360 resulta em uma reprodução de vídeo distorcida.

O visualizador foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. O visualizador suporta ferramentas opcionais de compartilhamento em redes sociais.

O visualizador Video360 usa a reprodução de vídeo de streaming HTML5 no formato HLS em sua configuração padrão sempre que o sistema subjacente suportar isso. Em sistemas que não suportam streaming HTML5, o visualizador volta ao delivery de vídeo progressivo HTML5.

O tipo de visualizador é 517.

## URLs de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

O HTML5 Video360 Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui com todos os componentes do HTML5 Viewer SDK usados por este visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

O HTML5 Video360 Viewer pode ser usado no modo de pop-up usando a página HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde é integrado à página da Web do público alvo usando a API documentada.

A configuração e a capa são semelhantes às dos outros visualizadores descritos neste guia. Toda a esfola é alcançada por meio de folhas de estilos em cascata personalizadas (CSS).

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

O conteúdo de vídeo 360 requer configurações de codificação mais altas do que o vídeo padrão não-360. Em outras palavras, o conteúdo 360 deve estar em maior resolução do que o vídeo não-360 para alcançar a mesma qualidade perceptível. É recomendável considerar as seguintes configurações de predefinição de vídeo adaptável para o vídeo 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Observe, no entanto, que a função de vídeo codificado com configurações de alta qualidade requer uma conexão de alta largura de banda no dispositivo do usuário final.

## Interação com o visualizador do Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

O HTML5 Video360 Viewer fornece um conjunto de controles padrão da interface do usuário para reprodução de vídeo, como botão reproduzir/pausar, bolha de tempo do vídeo do depurador de vídeo, indicador de tempo de reprodução/tempo total, controle de volume e botão de tela cheia. Todos esses controles são agrupados em barra de controle na parte inferior da interface do usuário do visualizador.

Observe que em dispositivos de toque o controle de volume fica oculto da interface do usuário, pois só é possível controlar o volume usando os botões de hardware do dispositivo.

Quando o visualizador opera no modo pop-up, um botão de tela cheia não está disponível na interface do usuário.

O visualizador também suporta diversas ferramentas de compartilhamento de mídia social. Eles estão disponíveis como um único botão na interface do usuário que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela. A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento suportado, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido às restrições de segurança do navegador da Web.

O visualizador suporta 360 reproduções de vídeo em fones de ouvido VR (como Oculus Go e Oculus Rift), montagens VR HMD (monitor montado na cabeça) (como o Google Cardboard) e dispositivos não habilitados para VR (como navegadores para desktop, tablets e telefones celulares não conectados a montagens VR HMD).

Nenhuma configuração adicional é necessária para visualização do conteúdo de vídeo 360 no fone de ouvido VR. O visualizador detecta automaticamente a presença de fone de ouvido VR e mostra o botão &quot;VR&quot; na parte superior do conteúdo de vídeo. A ativação deste botão &quot;VR&quot; muda a renderização do vídeo para o modo VR. O visualizador suporta renderização de VR somente em navegadores com suporte para WebVR.

Para usar montagens VR HMD, o modificador `Video360Player.vrrender` deve ser definido como `1` na configuração do visualizador, o que força a renderização estereoscópica.

Em fones de ouvido VR e montagens VR HMD, ocorre mudança de ponto de visualização em resposta ao movimento dos auscultadores, e nenhum outro controle de reprodução é fornecido no modo VR.

Ao assistir a vídeos 360 em dispositivos não habilitados para VR, o usuário final pode usar mouse, toque ou teclado para controlar a reprodução e o ponto de visualização do vídeo.

O visualizador suporta entrada de toque e entrada de mouse em dispositivos Windows com tela de toque e mouse, mas esse suporte é limitado apenas aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

O visualizador está totalmente acessível pelo teclado. Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando o visualizador Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsivo.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Na maioria dos casos, apenas um vídeo pode ser reproduzido por vez. Quando um usuário start reproduzindo um vídeo e tenta reproduzir outro, o primeiro vídeo é automaticamente pausado. O vídeo que foi pausado automaticamente lembra o tempo de reprodução atual, para que o usuário possa sempre voltar e retomar a reprodução. A única exceção desta regra é no navegador Chrome em dispositivos Android 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` chamada JavaScript, elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML predefinida para o modo de operação de pop-up. Ele é chamado [!DNL Video360Viewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão dos IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

A seguir está um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio de uma página da web.

Os casos de uso principal são páginas da Web orientadas para desktops ou tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web que têm um layout estático.

A incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à visualização, sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas de design da Web, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho que o layout da página da Web fornece. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir [!DNL Video360Viewer.js]. O arquivo [!DNL Video360Viewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal `include` na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca HTML5 SDK `Utils.js` carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o container `DIV`.

   Adicione um elemento vazio `DIV` à página onde deseja que o visualizador apareça. O elemento `DIV` deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   Para que o recurso de tela cheia funcione corretamente no Internet Explorer, verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento maior que o espaço reservado `DIV`.

   A seguir está um exemplo de um elemento de espaço reservado `DIV` definido:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático para o visualizador declarando-o para `.s7video360viewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no AEM Assets - sob demanda ou transmitido explicitamente usando o comando `style`.

   Consulte [Personalizando o visualizador Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro predefinido do visualizador no AEM Assets - sob demanda. Ou você pode passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params`, ou como uma chamada de API conforme descrito na seção Referência de comando, como:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.Video360Viewer`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração suportados pelo visualizador.

   Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem transmitido como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e start o visualizador com uma única linha de código, URL do servidor de vídeo passado como propriedade `videoserverurl`, ativo inicial como parâmetro `asset` e dados interativos como propriedade `interactivedata`. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o método `init()` logo antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso acontece, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. O exemplo considera o seguinte:

   * A instância do visualizador é `video360Viewer`.
   * O nome do espaço reservado `DIV` é `s7viewer`.
   * O URL de disponibilização de imagem é `https://s7d9.scene7.com/is/image`.
   * O URL do servidor de vídeo é `https://s7d9.scene7.com/is/content`.
   * O ativo é `Viewers/space_station_360-AVS`.

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o visualizador Video360 com um tamanho fixo:

   ```
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

Com incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita que o container do visualizador `DIV` tome 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web se parece com o seguinte:

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

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o DIV do container ao DIV `"holder"` existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

No caso de incorporação responsiva com largura e altura definidas, o estilo da página da Web é diferente. Fornece ambos os tamanhos para o `"holder"` DIV e centraliza-o na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%.

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

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

