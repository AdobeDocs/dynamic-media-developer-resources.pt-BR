---
title: Imagem interativa
description: O Visualizador de Imagens Interativas é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. O objetivo desse visualizador é implementar uma experiência de "banner que pode ser comprado". Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma página do Quickview ou de detalhes do produto em seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# Imagem interativa{#interactive-image}

O Visualizador de Imagens Interativas é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. O objetivo desse visualizador é implementar uma experiência de &quot;banner que pode ser comprado&quot;. Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma página do Quickview ou de detalhes do produto em seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador.

O tipo de visualizador é 508.

## URL de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do Visualizador de Imagem Interativa {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de Imagens Interativas representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Visualizador de imagens interativas pode ser usado somente no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e o skinning são semelhantes aos dos outros visualizadores descritos nesta Ajuda. Todo o esfolamento é obtido por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de Imagem Interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

A interação compatível com o Visualizador de imagem de vídeo é a ativação de ponto de acesso em sistemas de desktop. Essa ativação ocorre em dispositivos de clique e toque com um único toque.

O visualizador é totalmente acessível por teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando Visualizador de Imagem Interativa {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de Imagem Interativa é incorporado à página de hospedagem. Essa página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para tamanhos de janela de navegador diferentes.

Para acomodar essas necessidades, o visualizador aceita dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente. Esta página da Web pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas parte do imóvel de uma página da web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, e páginas projetadas responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação de design responsivo supõe que o visualizador deve ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolhe automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de web design, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preenche apenas essa área. Ele também segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do contêiner `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no HTML head. Antes de usar a API do visualizador, verifique se você incluiu [!DNL InterativeImage.js]. O [!DNL InteractiveImage.js] O arquivo está localizado sob a variável [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores da Adobe Dynamic Media Classic e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores da Adobe Dynamic Media Classic que têm os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
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

   Este é um exemplo de um espaço reservado definido `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7interactiveimage` classe CSS de nível superior em unidades absolutas ou usando `stagesize` modificador.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML. Ou você pode colocar o dimensionamento em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - On-demand ou passado explicitamente usando `style` comando.

   Consulte [Vídeo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre o estilo do visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Você pode transmitir explicitamente a variável `stagesize` modificador com o código de inicialização do visualizador com `params` ou como uma chamada de API, conforme descrito na seção Referência de comando , assim:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.InteractiveImage` classe , transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto deve ter `containerId` campo que contém o nome da ID do contêiner do visualizador e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador. Nesse caso, a variável `params` O objeto deve ter pelo menos o URL de disponibilização de imagens passado como `serverUrl` e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. Para ter compatibilidade máxima, chame a função `init()` método antes de fechar `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, pode estar oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando esse evento ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando a função `init()` método . O exemplo assume `interactiveImage` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` é o URL de disponibilização de imagens e `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` é o ativo:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de imagem de vídeo com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação responsiva do design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho de tempo de execução do contêiner do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita o contêiner do visualizador `DIV` para obter 40% do tamanho da janela do navegador da Web. E sua altura é deixada sem restrições. O código de HTML da página da Web seria semelhante ao seguinte:

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
1. Definição do contêiner `DIV`.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicionar o contêiner `DIV` aos `"holder"` `DIV`. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura irrestrita:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**Incorporação de tamanho flexível com definição de largura e altura**

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para a variável `"holder"` DIV e centralize-o na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%.

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
