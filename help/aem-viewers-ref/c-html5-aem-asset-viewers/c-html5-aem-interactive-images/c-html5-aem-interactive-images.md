---
title: Imagem interativa
description: O Visualizador de imagem interativo é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. A finalidade desse visualizador é implementar uma experiência de "banner para compra". Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma página de detalhes do produto ou de Quickview no seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1703'
ht-degree: 0%

---

# Imagem interativa{#interactive-image}

O Visualizador de imagem interativo é um visualizador que exibe uma única imagem sem zoom com pontos de acesso clicáveis. A finalidade desse visualizador é implementar uma experiência de &quot;banner para compra&quot;. Ou seja, o usuário pode selecionar um ponto de acesso sobre a imagem do banner e ser redirecionado para uma página de detalhes do produto ou de Quickview no seu site. Ele foi projetado para funcionar em desktops e dispositivos móveis.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são compatíveis com esse visualizador.

Tipo de visualizador 508.

## URL de demonstração {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Requisitos do sistema {#section-b7270cc4290043399681dc504f043609}

Consulte [Requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Uso do visualizador de imagem interativo {#section-e6c68406ecdc4de781df182bbd8088b4}

O Visualizador de imagem interativo representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única JavaScript inclui todos os componentes do SDK do Visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução.

O Visualizador de imagem interativo pode ser usado somente no modo incorporado, onde é integrado à página da Web de destino usando a API documentada.

A configuração e a aparência são semelhantes às dos outros visualizadores descritos nesta Ajuda. Toda a atribuição de capa é obtida por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o Visualizador de imagem interativo {#section-642e66ca38cd4032992840ec6c0b0cd2}

A interação suportada pelo Visualizador de imagem de vídeo é a ativação do ponto de acesso em sistemas desktop. Essa ativação ocorre em dispositivos de clique e toque com um único toque.

O visualizador é totalmente acessível pelo teclado.

Consulte [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporação do visualizador de imagens interativo {#section-6bb5d3c502544ad18a58eafe12a13435}

O Visualizador de imagem interativo é incorporado à página de hospedagem. Essa página da Web pode ter um layout estático ou pode ser &quot;responsiva&quot; e ser exibida de forma diferente em diferentes dispositivos ou para diferentes tamanhos de janela de navegador.

Para acomodar essas necessidades, o visualizador suporta dois modos de operação principais: incorporação de tamanho fixo e incorporação responsiva.

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente. Esta página da Web pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio imobiliário de uma página da Web.

Os principais casos de uso são páginas da Web orientadas para desktops ou dispositivos tablets e páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Esse método é a melhor opção para páginas da Web com layout estático.

A incorporação de design responsivo presume que o visualizador deve redimensionar em tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que usa um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente, dependendo da forma como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura irrestrita, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas responsivas de layout de design da Web, como Bootstrap e Foundation.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preencherá apenas essa área. Ela também segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é a incorporação do visualizador em uma sobreposição modal, em que a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Definindo o tamanho do visualizador.
1. Criar e inicializar o visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador exige a adição de uma tag de script no cabeçalho de HTML. Antes de usar a API do visualizador, inclua [!DNL InterativeImage.js]. O arquivo [!DNL InteractiveImage.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media Classic e for distribuído no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores do Adobe Dynamic Media Classic que têm os Visualizadores IS instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Faça referência somente ao arquivo `include` do visualizador principal do JavaScript na sua página. Não faça referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca `Utils.js` do SDK HTML5 carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas de visualizador de tempo de execução semelhantes é totalmente gerenciada pela lógica do visualizador e a localização muda entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, a inserção de uma referência direta a qualquer JavaScript `include` secundário usado pelo visualizador na página interrompe a funcionalidade do visualizador no futuro, quando uma nova versão do produto é implantada.

1. Definindo o container `DIV`.

   Adicione um elemento `DIV` vazio à página em que você deseja que o visualizador apareça. O elemento `DIV` deve ter sua ID definida porque essa ID é passada posteriormente para a API do visualizador. O DIV tem seu tamanho especificado por meio de CSS.

   O espaço reservado `DIV` é um elemento posicionado, o que significa que a propriedade CSS `position` está definida como `relative` ou `absolute`.

   Este é um exemplo de um elemento de espaço reservado `DIV` definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definir o tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para a classe CSS de nível superior `.s7interactiveimage` em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento em CSS diretamente na página do HTML. Ou você pode colocar o dimensionamento em um arquivo CSS do visualizador personalizado, que será posteriormente atribuído a um registro predefinido do visualizador no Adobe Experience Manager Assets - Sob demanda ou passado explicitamente usando o comando `style`.

   Consulte [Vídeo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático na página HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Você pode passar explicitamente o modificador `stagesize` com o código de inicialização do visualizador com a coleção `params` ou como uma chamada de API, conforme descrito na seção Referência de Comandos, desta forma:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Uma abordagem baseada em CSS é recomendada e é usada neste exemplo.

1. Criar e inicializar o visualizador.

   Quando tiver concluído as etapas acima, você criará uma instância da classe `s7viewers.InteractiveImage`, passará todas as informações de configuração para seu construtor e chamará o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto deve ter o campo `containerId`, que contém o nome da ID do contêiner de visualizador e o objeto JSON `params` aninhado com parâmetros de configuração com suporte do visualizador. Nesse caso, o objeto `params` deve ter pelo menos a URL do Servidor de imagens passada como propriedade `serverUrl`, e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante adicionar o contêiner do visualizador ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação do DOM até o fim da página da Web. Para obter compatibilidade máxima, chame o método `init()` antes de fechar a marca `BODY` ou no evento de corpo `onload()`.

   Ao mesmo tempo, o elemento de contêiner não deve necessariamente fazer parte do layout da página da Web ainda. Por exemplo, ela pode ser oculta usando o estilo `display:none` atribuído a ela. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando esse evento ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, passando opções de configuração mínimas necessárias para o construtor e chamando o método `init()`. O exemplo considera `interactiveImage` como a instância do visualizador; `s7viewer` como o nome do espaço reservado `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` como a URL do Servidor de Imagens e `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` como o ativo:

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

   O código a seguir é um exemplo completo de uma página da Web trivial que incorpora o Visualizador de imagem de vídeo com um tamanho fixo:

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

**Incorporação responsiva de design com altura irrestrita**

Com a incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho do tempo de execução do contêiner do visualizador `DIV`. Para o exemplo a seguir, considere que a página da Web permite que o contêiner do visualizador `DIV` ocupe 40% do tamanho da janela do navegador da Web. E sua altura é deixada irrestrita. O código de HTML da página da Web seria semelhante ao seguinte:

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

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o container `DIV`.
1. Criar e inicializar o visualizador.

Todas as etapas acima são as mesmas da incorporação de tamanho fixo. Adicionar o contêiner `DIV` ao `"holder"` `DIV` existente. O código a seguir é um exemplo completo. Observe como o tamanho do visualizador muda quando o navegador é redimensionado e como a taxa de proporção do visualizador corresponde ao ativo.

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

A página de exemplos a seguir ilustra mais usos reais da incorporação responsiva de design com altura irrestrita:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**Inserção de tamanho flexível com Largura e Altura Definidas**

Se houver incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web será diferente. Ele fornece ambos os tamanhos para o `"holder"` DIV e centralizá-lo na janela do navegador. Além disso, a página da Web define o tamanho do elemento `HTML` e `BODY` como 100%.

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

**Incorporando Usando API baseada em Setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor sem args. O uso deste construtor de API não aceita parâmetros e os parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

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
