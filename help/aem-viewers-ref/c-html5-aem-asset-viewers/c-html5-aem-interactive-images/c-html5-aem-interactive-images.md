---
description: O Interative Image Viewer é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. O objetivo deste visualizador é implementar uma experiência de "banner comprável". Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma Visualização rápida ou página de detalhes do produto em seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.
seo-description: O Interative Image Viewer é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. O objetivo deste visualizador é implementar uma experiência de "banner comprável". Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma Visualização rápida ou página de detalhes do produto em seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.
seo-title: Imagem interativa
solution: Experience Manager
title: Imagem interativa
topic: Dynamic Media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1806'
ht-degree: 0%

---


# Imagem interativa{#interactive-image}

O Interative Image Viewer é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. O objetivo deste visualizador é implementar uma experiência de &quot;banner comprável&quot;. Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma Visualização rápida ou página de detalhes do produto em seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador.

O tipo de visualizador é 508.

## URL de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Usando o Visualizador de Imagens Interativo {#section-e6c68406ecdc4de781df182bbd8088b4}

O Interative Image Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do Viewer SDK usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Interative Image Viewer pode ser usado somente no modo incorporado, onde é integrado à página da Web do público alvo usando a API documentada.

A configuração e o skinning são semelhantes aos outros visualizadores descritos nesta Ajuda. Todas as películas são obtidas por meio de CSS personalizado.

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador de Imagens Interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

A interação compatível com o Visualizador de imagens de vídeo é ativação de ponto de conexão em sistemas de desktop. Essa ativação ocorre em dispositivos de clique e toque com um único toque.

O visualizador está totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do Visualizador de Imagens Interativo {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de imagens interativo foi projetado para ser incorporado à página de hospedagem. Tal página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes.

Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente. Esta página da Web pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio de uma página da web.

Os casos de uso principal são páginas da Web orientadas para desktops ou tablets e páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web que têm um layout estático.

A incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à visualização, sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas de design da Web, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área. Ele também segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir [!DNL InterativeImage.js]. O arquivo [!DNL InteractiveImage.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
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

   A seguir está um exemplo de um elemento de espaço reservado `DIV` definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático para o visualizador declarando-o para `.s7interactiveimage` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento no CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no AEM Assets - sob demanda ou transmitido explicitamente usando o comando `style`.

   Consulte [Vídeo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Você pode passar explicitamente o modificador `stagesize` com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de comando, desta forma:

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.InteractiveImage`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração suportados pelo visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem transmitido como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o método `init()` logo antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir, há um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. O exemplo supõe que `interactiveImage` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` é o URL de disponibilização de imagem e `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` é o ativo:

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de imagens de vídeo com um tamanho fixo:

   ```
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

Com incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. No exemplo a seguir, suponha que a página da Web permita que o container do visualizador `DIV` tome 40% do tamanho da janela do navegador da Web. E sua altura é deixada sem restrições. O código HTML da página da Web se parece com o seguinte:

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
1. Definindo o container `DIV`.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o container `DIV` ao `"holder"` `DIV` existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**Incorporação de tamanho flexível com definição de largura e altura**

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Fornece ambos os tamanhos para o `"holder"` DIV e centraliza-o na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%.

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

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

