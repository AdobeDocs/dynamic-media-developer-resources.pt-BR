---
description: O Visualizador de vídeo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pelo Scene7 Publishing System ou AEM Dynamic Media.
keywords: responsive
seo-description: O Visualizador de vídeo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pelo Scene7 Publishing System ou AEM Dynamic Media.
seo-title: Vídeo
solution: Experience Manager
title: Vídeo
topic: Dynamic Media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '2402'
ht-degree: 0%

---


# Vídeo{#video}

O Visualizador de vídeo é um player de vídeo que reproduz streaming e vídeo progressivo codificado no formato H.264. Ele é fornecido pelo Scene7 Publishing System ou AEM Dynamic Media.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Vídeo único e Conjuntos de vídeo adaptáveis são suportados. Além disso, o visualizador oferece suporte ao trabalho com streams de vídeo progressivo e HLS hospedados em locais externos. Ele foi projetado para funcionar em navegadores da Web móveis e desktop que suportam vídeo HTML5. Este visualizador também oferece suporte a legendas ocultas opcionais que são exibidas sobre o conteúdo de vídeo, navegação por capítulo de vídeo e ferramentas de compartilhamento de mídia social.

O Visualizador de vídeo usa a reprodução de vídeo de streaming HTML5 no formato HLS em sua configuração padrão sempre que o sistema subjacente oferece suporte a ela. Em sistemas que não suportam streaming HTML5, o visualizador volta ao delivery de vídeo progressivo HTML5.

Tipo de visualizador 506.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Uso do Visualizador de vídeo {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de vídeo representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares - uma única inclusão do JavaScript com todos os componentes do Visualizador SDK usados por esse visualizador específico, ativos e CSS baixados pelo visualizador em tempo de execução.

Você pode usar o Visualizador de vídeo no modo pop-up usando a página HTML pronta para produção fornecida com os IS-Viewers. Ou você pode usar o visualizador no modo incorporado, onde ele é integrado a uma página da Web do público alvo usando a API documentada.

A tarefa de configurar e captar o visualizador é semelhante a outros visualizadores. Todas as películas são obtidas por meio de CSS personalizado.

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de vídeo {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de vídeo fornece um conjunto de controles padrão da interface do usuário para reprodução de vídeo, como um botão reproduzir/pausar, uma bolha de tempo do vídeo do depurador de vídeo, indicador de tempo de reprodução/tempo total, controle de volume, botão de tela cheia e alternância de legenda fechada. Todos esses controles são agrupados em uma barra de controle na parte inferior da interface do usuário do visualizador.

Em dispositivos de toque, o controle de volume fica oculto da interface do usuário, pois só é possível controlar o volume usando os botões de hardware.

Quando o visualizador opera no modo pop-up, o botão de tela cheia não está disponível na interface do usuário.

É possível navegar rapidamente no conteúdo de um vídeo quando a captação de vídeo é ativada. Os capítulos de vídeo são exibidos como marcadores na faixa do depurador de vídeo e mostram o título do capítulo e a descrição associada em uma rolagem do mouse sobre ou com um único toque em sistemas de toque. Os usuários podem buscar um capítulo específico clicando em um marcador de capítulo ou tocando na bolha de descrição do capítulo.

O visualizador suporta a entrada de toque e a entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Este visualizador está totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Ferramentas de compartilhamento de mídia social com o Visualizador de vídeo {#section-907d316fe1da4b87abb9775f02464704}

O Visualizador de vídeo suporta ferramentas de compartilhamento de mídia social Eles estão disponíveis como um único botão na interface do usuário, que se expande em uma barra de ferramentas de compartilhamento quando o usuário clica ou toca nele.

A barra de ferramentas de compartilhamento contém um ícone para cada tipo de canal de compartilhamento suportado, como Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter são chamados, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão a partir de um serviço de mídia social. Além disso, quando uma ferramenta de compartilhamento é ativada, a reprodução de vídeo é pausada automaticamente.

As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido às restrições de segurança do navegador da Web.

## Incorporando o Visualizador de Vídeo {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsivo.

A incorporação de vários vídeos na mesma página é compatível com tablets e dispositivos móveis. Na maioria dos casos, apenas um vídeo pode ser reproduzido por vez. Quando um usuário start reproduzindo um vídeo e tenta reproduzir outro, o primeiro vídeo é automaticamente pausado. O vídeo que foi pausado automaticamente lembra o tempo de reprodução atual, para que o usuário possa sempre voltar e retomar a reprodução. A única exceção desta regra é no navegador Chrome em dispositivos Android 4.x, que podem reproduzir vídeos em paralelo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação do dispositivo seja alterada.

Esse modo é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` chamada JavaScript, elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML predefinida para o modo de operação de pop-up. Ele é chamado [!DNL VideoViewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão dos IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

A seguir está um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio da página.

O caso de uso principal são páginas da Web orientadas para desktops ou tablets, e também páginas de design responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é a melhor para páginas da Web que têm um layout de página estático.

A incorporação responsiva do design supõe que o visualizador pode precisar redimensionar em tempo de execução em resposta à alteração do tamanho de seu container `DIV`. O caso de uso mais comum é adicionar o visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Esse método garante que o ativo se ajuste perfeitamente à visualização sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam uma estrutura de layout de design responsivo, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir [!DNL FlyoutViewer.js]. O arquivo [!DNL FlyoutViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo é semelhante ao seguinte:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal `include` na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca HTML5 SDK `Utils.js` carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o DIV do container.

   Adicione um elemento DIV vazio à página onde deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois ela é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio do CSS.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   Verifique se o recurso de tela cheia funciona corretamente no Internet Explorer. Verifique se não há outros elementos no DOM que tenham uma ordem de empilhamento superior à do espaço reservado DIV.

   A seguir está um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7videoviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Scene7 Publishing System ou transmitido explicitamente usando um comando de estilo.

   Consulte [Personalizar o Visualizador de vídeo](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) para obter mais informações sobre como estilizar o visualizador usando CSS.

   A seguir está um exemplo de como definir um tamanho de visualizador estático em uma página HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro predefinido do visualizador no Scene7 Publishing System, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params`, ou como uma chamada de API conforme descrito na seção Referência de comando, como a seguir:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.VideoViewer`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração suportados pelo visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem passado como propriedade `serverUrl`, o URL do servidor de vídeo passado como propriedade `videoserverurl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o método `init()` logo antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. Este exemplo supõe que `videoViewer` é a instância do visualizador, `s7viewer` é o nome do espaço reservado `DIV`, [!DNL http://s7d1.scene7.com/is/image/] é o URL de disponibilização de imagem, [!DNL http://s7d1.scene7.com/is/content/] é o URL do servidor de vídeo e [!DNL Scene7SharedAssets/Glacier_Climber_MP4] é o ativo.

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

Com a incorporação do design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita que o container do visualizador `DIV` pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web se parece com o seguinte:

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

Adicionar o visualizador a uma página desse tipo é muito semelhante à incorporação de tamanho fixo; a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o DIV do container.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o container `DIV` ao &quot; detentor&quot; `DIV` existente. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

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

A página de exemplos a seguir ilustra o uso mais real da incorporação responsiva de design com altura sem restrições:

[Demos ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporação de design responsivo com definição de largura e altura**

No caso de incorporação de design responsivo com largura e altura definidas, o estilo da página da Web é diferente; fornece ambos os tamanhos para o &quot; holder&quot; `DIV` e centraliza-o na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%:

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

As etapas de incorporação restantes são idênticas à incorporação de design responsivo com altura irrestrita. O exemplo resultante é o seguinte:

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

**Como incorporar usando a API baseada em Setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com essa API, o construtor não aceita parâmetros e parâmetros de configuração são especificados usando os métodos `setContainerId()`, `setParam()` e `setAsset()` da API com chamadas JavaScript separadas.

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

