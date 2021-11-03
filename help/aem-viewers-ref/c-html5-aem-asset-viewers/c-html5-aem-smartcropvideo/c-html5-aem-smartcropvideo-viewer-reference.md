---
title: Vídeo de recorte inteligente
description: O Smart Crop Video Viewer é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264 com a adição de suporte para recorte inteligente. Ele é fornecido pela Dynamic Media Classic ou Adobe Experience Manager com o Dynamic Media.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '2410'
ht-degree: 0%

---

# Vídeo{#video}

O Smart Crop Video Viewer é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264 com a adição de suporte para recorte inteligente. Ele é fornecido pelo Dynamic Media Classic ou Experience Manager com o Dynamic Media.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Vídeo único e Conjuntos de vídeo adaptativo são suportados. Além disso, o visualizador aceita trabalhar com fluxos de vídeo progressivos e HLS hospedados em locais externos. Ele foi projetado para funcionar em navegadores para desktop e dispositivos móveis da Web que suportam vídeo HTML5. Esse visualizador também oferece suporte a legendas ocultas opcionais exibidas sobre conteúdo de vídeo, navegação de capítulo de vídeo e ferramentas de compartilhamento de redes sociais.

O Smart Crop Video Viewer usa a reprodução de vídeo de transmissão HTML5 no formato HLS em sua configuração padrão, sempre que o sistema subjacente oferece suporte para isso. Em sistemas que não suportam streaming de HTML5, o visualizador volta para a entrega de vídeo progressivo do HTML5.

Tipo de visualizador 518.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## Usar o visualizador de vídeo de recorte inteligente {#section-f21ac23d3f6449ad9765588d69584772}

O Smart Crop Video Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares - uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos e CSS baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de vídeo de recorte inteligente no modo pop-up usando a página HTML pronta para produção fornecida com os IS-Viewers. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado em uma página da Web de destino usando a API documentada.

A tarefa de configurar e esfolar o visualizador é semelhante a outros visualizadores. Todo o esfolamento é obtido por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de vídeo de recorte inteligente {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Smart Crop Video Viewer fornece um conjunto de controles padrão da interface do usuário para a reprodução do vídeo, como:

* Um botão Reproduzir/Pausar.
* Bolha de tempo do vídeo do depurador de vídeo.
* Indicador de tempo/tempo total reproduzido.
* Controle de volume.
* Botão de tela cheia.
* Alternância de legenda fechada.

Todos esses controles são agrupados em uma barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware.

Quando o visualizador opera no modo pop-up, o botão de tela cheia não está disponível na interface do usuário.

É possível navegar pelo conteúdo de um vídeo rapidamente quando o capítulo de vídeo está ativado. Os capítulos de vídeo são exibidos como marcadores na faixa do depurador de vídeo e mostram o título do capítulo e a descrição associada em uma rolagem do mouse ou com um único toque nos sistemas de toque. Os usuários podem buscar um capítulo específico selecionando um marcador de capítulo ou a bolha de descrição do capítulo.

O visualizador aceita entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Esse visualizador é totalmente acessível por teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Ferramentas de compartilhamento em redes sociais com o Visualizador de vídeo de recorte inteligente {#section-907d316fe1da4b87abb9775f02464704}

O Smart Crop Video Viewer oferece suporte às ferramentas de compartilhamento de mídia social. Eles estão disponíveis como um único botão na interface do usuário, que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela.

A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento de incorporação ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente.

O compartilhamento de ferramentas não está disponível no modo de tela cheia devido a restrições de segurança do navegador da Web.

## Como incorporar o visualizador de vídeo de recorte inteligente {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Geralmente, apenas um vídeo pode ser reproduzido de cada vez. Quando um usuário começa a reproduzir um vídeo e tenta reproduzir outro, o primeiro é pausado automaticamente. O vídeo que foi pausado automaticamente lembra do tempo de reprodução atual, para que o usuário possa sempre retornar a ele e retomar a reprodução. A única exceção desta regra é no navegador Chrome em dispositivos Android™ 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` Chamada de JavaScript, configurada corretamente `A` HTML ou qualquer outro método adequado.

É recomendável usar uma página de HTML pronta para uso no modo de operação pop-up. É chamado de [!DNL SmartCropVideoViewer.html] e está localizado sob a [!DNL html5/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. Normalmente, o visualizador ocupa apenas parte do imóvel da página.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, e também páginas de design responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor para páginas da Web que têm um layout de página estático.

A incorporação responsiva de design supõe que o visualizador deve ser redimensionado em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar o visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo de como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolhe automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Esse método garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam uma estrutura de layout de design responsivo, como Bootstrap ou Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preenche apenas essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no HTML head. Antes de usar a API do visualizador, verifique se você incluiu [!DNL SmartCropVideoViewer.js]. O [!DNL SmartCropVideoViewer.js] O arquivo está localizado sob a variável [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores da Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores da Adobe Dynamic Media Classic que têm os IS-Viewers instalados.

O caminho relativo é semelhante ao seguinte:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   Certifique-se de que o recurso de tela cheia funcione corretamente no Internet Explorer. Verifique para garantir que não haja outros elementos no DOM que tenham uma ordem de empilhamento mais alta do que o DIV do espaço reservado.

   Este é um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7videoviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado. Posteriormente, ele é atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou passado explicitamente usando um comando style.

   Consulte [Personalizar o visualizador de vídeo de recorte inteligente](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obter mais informações sobre o estilo do visualizador usando CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático em uma página de HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir `stagesize` modificador no registro predefinido do visualizador no Dynamic Media Classic ou passe-o explicitamente com o código de inicialização do visualizador com `params` coleção. Ou, como uma chamada de API, conforme descrito na seção Referência de comando , como em:

   ```
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.SmartCropVideoViewer` classe , transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter `containerId` campo que contém o nome da ID do contêiner do visualizador e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador. Nesse caso, `params` O objeto deve ter pelo menos o URL de disponibilização de imagens passado como `serverUrl` propriedade, URL do servidor de vídeo passado como `videoserverurl` e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame a função `init()` método antes de fechar `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, pode estar oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando a função `init()` método . Este exemplo supõe `smartCropVideoViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagens, [!DNL http://s7d1.scene7.com/is/content/] é o URL do servidor de vídeo e [!DNL html5automation/frisbee-AVS] é o ativo.

   ```
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de Vídeo de Corte Inteligente com um tamanho fixo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação do design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita o contêiner do visualizador `DIV` para obter 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código de HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante à incorporação de tamanho fixo; a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicionar contêiner `DIV` ao atual &quot;detentor&quot; `DIV`. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

As etapas de incorporação restantes são idênticas à incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
