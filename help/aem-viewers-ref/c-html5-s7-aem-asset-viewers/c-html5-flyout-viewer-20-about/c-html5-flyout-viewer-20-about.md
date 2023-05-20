---
title: Flyout
description: O Visualizador de imagem suspensa é um visualizador de imagem. Ela exibe uma imagem estática com a versão com zoom mostrada na visualização da imagem suspensa que um usuário ativa. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# Flyout{#flyout}

O Visualizador de imagem suspensa é um visualizador de imagem. Ela exibe uma imagem estática com a versão com zoom mostrada na visualização da imagem suspensa que um usuário ativa. Esse visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador.

Tipo de visualizador 504.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilização do visualizador de imagem suspensa {#section-f21ac23d3f6449ad9765588d69584772}

O Visualizador de imagem suspensa representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (um único JavaScript inclui todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução

O Visualizador de imagem suspensa se destina apenas ao uso incorporado, o que significa que ele é integrado à página da Web usando a API documentada. Nenhuma página da Web pronta para produção está disponível para o Visualizador de imagem suspensa.

A configuração e a aparência são semelhantes às dos outros visualizadores. Você pode usar CSS personalizado para aplicar a atribuição de capa.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o visualizador de imagem suspensa {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Visualizador de imagem suspensa é compatível com gestos de toque único e multitoque comuns em outros aplicativos móveis.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Toque único </p> </td> 
   <td colname="col2"> <p> Ativa a exibição de imagem suspensa ou altera entre os níveis de zoom primário e secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou mover horizontalmente </p> </td> 
   <td colname="col2"> <p> Rola pela lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deslizamento vertical </p> </td> 
   <td colname="col2"> <p>Se o gesto for feito na área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada por toque e à entrada do mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte está limitado apenas aos navegadores Chrome, Internet Explorer 11 e Edge.

Este visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação pelo teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de imagem suspensa {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. A página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela de navegador. Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação de design responsiva.

O modo de incorporação de tamanho fixo é usado quando o visualizador não altera seu tamanho após o carregamento inicial. Essa opção é melhor para páginas da Web com layout de página estático.

O modo de incorporação de design responsivo presume que o visualizador deve redimensionar durante o tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

Ao usar o modo de incorporação de design responsivo com o Visualizador de imagem suspensa, especifique pontos de interrupção explícitos para a imagem de exibição principal usando o `imagereload` parâmetro. Idealmente, associe seus pontos de interrupção com os pontos de interrupção de largura do visualizador, conforme ditado pelo CSS da página da Web.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como um contêiner de página da Web `DIV` é dimensionado. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura irrestrita, o visualizador escolhe automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade significa que o ativo se encaixa perfeitamente na exibição sem qualquer preenchimento nas laterais. Esse caso de uso específico é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preenche somente essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo de caso de uso é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do contêiner `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua `FlyoutViewer.js`. `FlyoutViewer.js` está no seguinte [!DNL html5/js/] subpasta da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media e for distribuído no mesmo domínio. Caso contrário, você especificará um caminho completo para um dos servidores Adobe Dynamic Media que possuem os Visualizadores IS instalados.

Um caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Fazer referência apenas ao JavaScript do visualizador principal `include` arquivo na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Em particular, não faça referência direta ao SDK do HTML5 `Utils.js` biblioteca carregada pelo visualizador de `/s7viewers` caminho de contexto (o chamado SDK consolidado) `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução são totalmente gerenciadas pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões mais antigas do visualizador secundário `includes` no servidor.
>
>
>Como resultado, ao inserir uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definição do container DIV.

   Adicione um elemento DIV vazio à página em que você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que o `position` A propriedade CSS está definida como `relative` ou `absolute`.

   É responsabilidade da página da Web especificar as `z-index` para o elemento DIV do espaço reservado. Isso garante que a parte da imagem suspensa do visualizador apareça sobre os outros elementos da página da Web.

   Veja a seguir um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Definindo o tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Nos sistemas desktop, as miniaturas são colocadas abaixo da exibição principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando `setAsset()` API. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na área inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e permitir que a exibição principal aumente sua altura e ocupe a área de miniaturas. Ou você pode manter o tamanho de exibição principal estático e recolher a área do visualizador externo, permitindo que o conteúdo da página da Web se mova para cima e usar o espaço livre da página deixado nas miniaturas.

   Para manter intactos os limites do visualizador externo, defina o tamanho para `.s7flyoutviewer` classe CSS de nível superior em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado, posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic ou passado explicitamente usando o comando style.

   Consulte [Personalização do visualizador de imagem suspensa](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obter mais informações sobre como estilizar o visualizador com CSS.

   Veja a seguir um exemplo de definição do tamanho estático do visualizador externo em uma página de HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na página de exemplo a seguir. Observe que, ao alternar entre conjuntos, o tamanho do visualizador externo não é alterado:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Para tornar as dimensões de exibição principais estáticas, defina o tamanho do visualizador em unidades absolutas para o painel interno `Container` Componente do SDK usando `.s7flyoutviewer .s7container` Seletor de CSS. Além disso, você deve substituir o tamanho fixo definido para o `.s7flyoutviewer` classe CSS de nível superior no CSS do visualizador padrão, configurando-a para `auto`.

   Veja a seguir um exemplo de definição do tamanho do visualizador para o `Container` Componente do SDK para que a área de exibição principal não altere o tamanho ao alternar o ativo:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de exemplo a seguir mostra o comportamento do visualizador com um tamanho de exibição principal fixo. Observe que quando você alternar entre conjuntos, a exibição principal permanecerá estática e o conteúdo da página da Web se moverá verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Além disso, o CSS do visualizador padrão fornece um tamanho fixo para sua área externa pronta para uso.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância de `s7viewers.FlyoutViewer` classe, transmita todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter a `containerId` campo que contém o nome da ID do contêiner de visualização e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador. Neste caso, o `params` objeto deve ter pelo menos o URL do Servidor de imagens passado como `serverUrl` propriedade e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o `init()` método antes do fechamento `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, pode ser oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação acontece, o carregamento do visualizador é retomado automaticamente.

   Veja a seguir um exemplo de criação de uma instância do visualizador, passando as opções de configuração mínimas necessárias para o construtor e chamando o `init()` método. O exemplo assume `flyoutViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` é o URL do Servidor de Imagens; e `Scene7SharedAssets/ImageSet-Views-Sample` é o ativo:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de imagem suspensa com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporação responsiva de design com altura irrestrita {#section-056cb574713c4d07be6d07cf3c598839}

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

Adicionar o visualizador a essa página é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você deve substituir o tamanho fixo do CSS do visualizador padrão pelo tamanho definido em unidades relativas.

1. Adicionar o arquivo JavaScript do visualizador à página da Web.
1. Definição do contêiner `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo, com as três exceções a seguir:

* adicionar o contêiner `DIV` ao &quot;detentor&quot; existente `DIV`;
* adicionado `imagereload` parâmetro com pontos de interrupção explícitos;
* em vez de definir um tamanho fixo do visualizador usando unidades absolutas, use o CSS que define a largura e a altura do visualizador como 100%, como no exemplo a seguir:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Local de demonstração alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incorporação de tamanho flexível com largura e altura definidas {#section-0a329016f9414d199039776645c693de}

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centraliza na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%.

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

O restante das etapas de incorporação são idênticas às etapas usadas para incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporação usando a API baseada em setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`, e `setAsset()` Métodos de API do, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
