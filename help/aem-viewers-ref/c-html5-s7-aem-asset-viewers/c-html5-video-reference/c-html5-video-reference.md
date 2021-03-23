---
description: O Visualizador de vídeo é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pelo Dynamic Media Classic ou AEM Dynamic Media.
keywords: responsivo
solution: Experience Manager
title: Vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# Vídeo{#video}

O Visualizador de vídeo é um reprodutor de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pelo Dynamic Media Classic ou AEM Dynamic Media.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Vídeo único e Conjuntos de vídeo adaptativo são suportados. Além disso, o visualizador aceita trabalhar com fluxos de vídeo progressivos e HLS hospedados em locais externos. Ele foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. Esse visualizador também oferece suporte a legendas ocultas opcionais exibidas sobre conteúdo de vídeo, navegação de capítulo de vídeo e ferramentas de compartilhamento de redes sociais.

O Visualizador de vídeo usa a reprodução de vídeo de streaming HTML5 no formato HLS em sua configuração padrão, sempre que o sistema subjacente oferece suporte a ela. Em sistemas que não suportam streaming HTML5, o visualizador volta para a entrega de vídeo progressivo HTML5.

Tipo de visualizador 506.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Uso do visualizador de vídeo {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de vídeo representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares - uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos e CSS baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de vídeo no modo pop-up usando a página HTML pronta para produção fornecida com os IS-Viewers. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado em uma página da Web de destino usando a API documentada.

A tarefa de configurar e esfolar o visualizador é semelhante a outros visualizadores. Todo o esfolamento é obtido por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de vídeo {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de vídeo fornece um conjunto de controles padrão da interface do usuário para a reprodução do vídeo, como um botão Reproduzir/Pausar, bolha de tempo do vídeo do depurador de vídeo, indicador de tempo de reprodução/tempo total, controle de volume, botão de tela cheia e alternância de legenda fechada. Todos esses controles são agrupados em uma barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto na interface do usuário, pois só é possível controlar o volume usando os botões de hardware.

Quando o visualizador opera no modo pop-up, o botão de tela cheia não está disponível na interface do usuário.

É possível navegar pelo conteúdo de um vídeo rapidamente quando a filtragem de vídeo está ativada. Os capítulos de vídeo são exibidos como marcadores no rastreamento do depurador de vídeo e mostram o título do capítulo e a descrição associada em um roll-over do mouse ou com um único toque em sistemas de toque. Os usuários podem buscar um capítulo específico clicando em um marcador de capítulo ou tocando na bolha de descrição do capítulo.

O visualizador aceita entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Esse visualizador é totalmente acessível por teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Ferramentas de compartilhamento de redes sociais com o Visualizador de vídeo {#section-907d316fe1da4b87abb9775f02464704}

O Visualizador de vídeo é compatível com ferramentas de compartilhamento de mídia social. Eles estão disponíveis como um único botão na interface do usuário, que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nela.

A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento compatível, como Facebook, Twitter, compartilhamento de email, compartilhamento de código de incorporação e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento de incorporação ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente.

O compartilhamento de ferramentas não está disponível no modo de tela cheia devido a restrições de segurança do navegador da Web.

## Incorporando visualizador de vídeo {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. Neste último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Na maioria dos casos, apenas um vídeo pode ser reproduzido por vez. Quando um usuário começa a reproduzir um vídeo e tenta reproduzir outro, o primeiro é pausado automaticamente. O vídeo que foi pausado automaticamente lembra do tempo de reprodução atual, para que o usuário possa sempre retornar a ele e retomar a reprodução. A única exceção desta regra é no navegador Chrome em dispositivos Android 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando a chamada `window.open()` do JavaScript, o elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML predefinida para o modo de operação pop-up. Ele é chamado [!DNL VideoViewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. Normalmente, o visualizador ocupa apenas parte do imóvel da página.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, e também páginas de design responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor para páginas da Web que têm um layout de página estático.

A incorporação responsiva de design supõe que o visualizador talvez precise ser redimensionado em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar o visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo de como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Esse método garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam uma estrutura de layout de design responsivo, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, inclua [!DNL FlyoutViewer.js]. O arquivo [!DNL FlyoutViewer.js] está localizado na subpasta [!DNL html5/js/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic que tenham os IS-Viewers instalados.

O caminho relativo é semelhante ao seguinte:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript `include` do visualizador principal na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador em tempo de execução. Em particular, não faça referência diretamente à biblioteca de SDK `Utils.js` HTML5 carregada pelo visualizador do `/s7viewers` caminho de contexto (o chamado SDK consolidado `include`). O motivo é que o local de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciado pela lógica do visualizador e o local muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão de produto for implantada.

1. Definição do DIV do contêiner.

   Adicione um elemento DIV vazio à página onde você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O DIV de espaço reservado é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Certifique-se de que o recurso de tela cheia funcione corretamente no Internet Explorer. Verifique para garantir que não haja outros elementos no DOM que tenham uma ordem de empilhamento mais alta do que o DIV do espaço reservado.

   Este é um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7videoviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou passado explicitamente usando um comando style.

   Consulte [Personalização do visualizador de vídeo](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obter mais informações sobre o estilo do visualizador usando CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático em uma página HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir `stagesize` modificador no registro de predefinição do visualizador no Dynamic Media Classic, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API conforme descrito na seção Referência de comandos , como em:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Após concluir as etapas acima, crie uma instância de `s7viewers.VideoViewer` classe, passe todas as informações de configuração para seu construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do contêiner do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de Exibição de Imagem passado como propriedade `serverUrl`, o URL do servidor de vídeo passado como propriedade `videoserverurl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame o método `init()` antes de fechar a tag `BODY` ou no evento body `onload()` .

   Ao mesmo tempo, o elemento do contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir, um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando o método `init()`. Este exemplo supõe que `videoViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagem, [!DNL http://s7d1.scene7.com/is/content/] é o URL do servidor de vídeo e [!DNL Scene7SharedAssets/Glacier_Climber_MP4] é o ativo.

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de vídeo com um tamanho fixo:

   ```
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

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação do design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita que o contêiner do visualizador `DIV` pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web seria semelhante ao seguinte:

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

Adicionar o visualizador a essa página é muito semelhante à incorporação de tamanho fixo; a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o contêiner `DIV` ao &quot; detentor&quot; existente `DIV`. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

A página de exemplos a seguir ilustra o uso mais real da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporação de design responsivo com largura e altura definidas**

No caso de incorporação de design responsivo com largura e altura definidas, o estilo da página da Web é diferente; ele fornece ambos os tamanhos ao &quot; holder&quot; `DIV` e centraliza na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` para 100%:

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

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com essa API, o construtor não utiliza parâmetros e parâmetros de configuração são especificados usando `setContainerId()`, `setParam()` e `setAsset()` métodos de API com chamadas JavaScript separadas.

O exemplo a seguir ilustra a incorporação de tamanho fixo com a API baseada em setter:

```
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

