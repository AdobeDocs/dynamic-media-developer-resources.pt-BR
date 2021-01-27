---
description: O Flyout Viewer é um visualizador de imagens. Ele exibe uma imagem estática com a versão ampliada mostrada na visualização de flyout que um usuário ativa. Este visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.
keywords: responsive
solution: Experience Manager
title: Flyout
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 0%

---


# Flyout{#flyout}

O Flyout Viewer é um visualizador de imagens. Ele exibe uma imagem estática com a versão ampliada mostrada na visualização de flyout que um usuário ativa. Este visualizador funciona com conjuntos de imagens e a navegação é feita usando amostras. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador.

O tipo de visualizador é 504.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Usando o Flyout Viewer {#section-f21ac23d3f6449ad9765588d69584772}

O Flyout Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do Viewer SDK usados por este visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução

O Flyout Viewer destina-se apenas ao uso incorporado, o que significa que ele está integrado à página da Web usando a API documentada. Nenhuma página da Web pronta para produção está disponível para o Flyout Viewer.

A configuração e a capa são semelhantes às dos outros visualizadores. Você pode usar CSS personalizado para aplicar capas.

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Flyout Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

O Flyout Viewer suporta gestos de toque único e multitoque que são comuns em outros aplicativos móveis.

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
   <td colname="col2"> <p> Ativa a visualização de flyout ou as alterações entre o nível de zoom primário e secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque horizontal ou toque </p> </td> 
   <td colname="col2"> <p> Percorre a lista de amostras na barra de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque vertical </p> </td> 
   <td colname="col2"> <p>Se o gesto for feito dentro da área de amostras, ele executará uma rolagem de página nativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

O visualizador também oferece suporte à entrada de toque e à entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Este visualizador está totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporando o Flyout Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. A página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação de design responsivo.

O modo de incorporação de tamanho fixo é usado quando o visualizador não altera seu tamanho após a carga inicial. Essa opção é melhor para páginas da Web que tenham um layout de página estático.

O modo de incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado durante o tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

Ao usar o modo de incorporação de design responsivo com o Flyout Viewer, certifique-se de especificar pontos de interrupção explícitos para a imagem de visualização principal usando o parâmetro `imagereload`. Idealmente, combine seus pontos de interrupção com os pontos de interrupção da largura do visualizador, conforme indicado pelo CSS da página da Web.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como uma página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Isso significa que o ativo se encaixa perfeitamente na visualização, sem qualquer preenchimento lateral. Esse caso de uso em particular é o mais comum para páginas da Web que usam estruturas de layout de design responsivas, como Bootstrap, Base e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá somente essa área e seguirá o tamanho fornecido pelo layout da página da Web. Um bom exemplo de caso de uso é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir `FlyoutViewer.js`. `FlyoutViewer.js` está localizado na seguinte  [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media e ele for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media com os IS-Viewers instalados.

Um caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal `include` na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca HTML5 SDK `Utils.js` carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o DIV do container.

   Adicione um elemento DIV vazio à página onde deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   É responsabilidade da página da Web especificar o `z-index` apropriado para o elemento DIV do espaço reservado. Isso garante que a parte de flyout do visualizador apareça na parte superior dos outros elementos da página da Web.

   A seguir está um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Definição do tamanho do visualizador.

   Este visualizador exibe miniaturas ao trabalhar com conjuntos de vários itens. Em sistemas desktop, as miniaturas são colocadas abaixo da visualização principal. Ao mesmo tempo, o visualizador permite a troca do ativo principal durante o tempo de execução usando a API `setAsset()`. Como desenvolvedor, você tem controle sobre como o visualizador gerencia a área de miniaturas na área inferior quando o novo ativo tem apenas um item. É possível manter o tamanho do visualizador externo intacto e deixar a visualização principal aumentar sua altura e ocupar a área de miniaturas. Ou você pode manter o tamanho da visualização principal estático e reduzir a área do visualizador externo, permitindo, assim, que o conteúdo da página da Web se mova para cima e, em seguida, usar o espaço livre da página nas miniaturas.

   Para manter os limites do visualizador externo intactos, defina o tamanho para `.s7flyoutviewer` classe CSS de nível superior em unidades absolutas. O dimensionamento no CSS pode ser colocado diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Scene7 Publishing System, ou transmitido explicitamente usando o comando style.

   Consulte [Personalizando o Flyout Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir o tamanho do visualizador externo estático em uma página HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode ver o comportamento com uma área fixa do visualizador externo na seguinte página de amostra. Observe que quando você alterna entre os conjuntos, o tamanho do visualizador externo não muda:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Para tornar as dimensões de visualização principais estáticas, defina o tamanho do visualizador em unidades absolutas para o componente SDK interno `Container` usando o seletor de CSS `.s7flyoutviewer .s7container`. Além disso, você deve substituir o tamanho fixo definido para a classe CSS `.s7flyoutviewer` de nível superior no CSS do visualizador padrão, definindo-o como `auto`.

   A seguir está um exemplo de como definir o tamanho do visualizador para o componente SDK interno `Container` para que a área de visualização principal não altere seu tamanho ao alternar o ativo:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   A página de amostra a seguir mostra o comportamento do visualizador com um tamanho de visualização principal fixo. Observe que quando você alterna entre os conjuntos, a visualização principal permanece estática e o conteúdo da página da Web se move verticalmente:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Além disso, observe que o CSS do visualizador padrão fornece um tamanho fixo para sua área externa pronta para uso.

1. Criação e inicialização do visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.FlyoutViewer`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração compatíveis com o visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem transmitido como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. Para obter compatibilidade máxima, chame o método `init()` logo antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. O exemplo supõe que `flyoutViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` é o URL de disponibilização de imagens; e `Scene7SharedAssets/ImageSet-Views-Sample` é o ativo:

   ```
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

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Flyout Viewer com um tamanho fixo:

   ```
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

## Incorporação de design responsivo com altura sem restrições {#section-056cb574713c4d07be6d07cf3c598839}

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

Adicionar o visualizador a uma página assim é semelhante às etapas para incorporação de tamanho fixo. A única diferença é que você precisa substituir o dimensionamento fixo do CSS do visualizador padrão pelo tamanho definido em unidades relativas.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo com as três exceções a seguir:

* adicionar o container `DIV` ao &quot;detentor&quot; existente `DIV`;
* foi adicionado o parâmetro `imagereload` com pontos de interrupção explícitos;
* em vez de definir um tamanho fixo do visualizador usando unidades absolutas, use o CSS que define a largura e a altura do visualizador como 100%, como a seguir:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
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

A página de exemplos a seguir ilustra os usos mais reais da incorporação responsiva de design com altura irrestrita:

[Demos ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Incorporação flexível de tamanho com largura e altura definidas {#section-0a329016f9414d199039776645c693de}

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%.

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

O restante das etapas de incorporação são idênticos às etapas usadas para incorporação de design responsivo com altura irrestrita. O exemplo resultante é o seguinte:

```
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

## Incorporação usando a API baseada em Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. O uso desse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()`, com chamadas JavaScript separadas.

O exemplo a seguir ilustra o uso da incorporação de tamanho fixo com a API baseada em setter:

```
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

