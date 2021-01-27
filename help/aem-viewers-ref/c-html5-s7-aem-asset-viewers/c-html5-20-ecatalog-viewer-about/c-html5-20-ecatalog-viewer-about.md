---
description: O eCatalog Viewer é um visualizador de catálogo que exibe folhetos eletrônicos em uma página espelhada ou página por página, O eCatalog permite que os usuários naveguem pelo catálogo usando elementos adicionais da interface do usuário ou modo de miniaturas dedicado. Os usuários também podem aumentar o zoom em cada página para obter mais detalhes.
keywords: responsive
solution: Experience Manager
title: eCatalog
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '2163'
ht-degree: 0%

---


# eCatalog{#ecatalog}

O eCatalog Viewer é um visualizador de catálogo que exibe folhetos eletrônicos em uma página espelhada ou página por página, O eCatalog permite que os usuários naveguem pelo catálogo usando elementos adicionais da interface do usuário ou modo de miniaturas dedicado. Os usuários também podem aumentar o zoom em cada página para obter mais detalhes.

>[!NOTE]
>
>As imagens que usam a renderização de imagem (IR) ou o conteúdo gerado pelo usuário (UGC) não são suportadas por este visualizador.

Tipo de visualizador 507.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Esse visualizador funciona com ecatalogs e oferece suporte a mapas de imagem opcionais e ferramentas de compartilhamento em redes sociais. Ele tem ferramentas de zoom, ferramentas de navegação de catálogo, suporte a tela cheia, miniaturas e um botão de fechamento opcional. O visualizador também suporta ferramentas de compartilhamento em redes sociais, Imprimir, Download e Favoritos. Ele foi projetado para funcionar em desktops e dispositivos móveis.

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## Usando o eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

O eCatalog Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do Viewer SDK usados por este visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução

Você pode usar o eCatalog Viewer no modo pop-up usando uma página HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde é integrado à página da Web do público alvo usando API documentada.

A configuração e a capa são semelhantes às dos outros visualizadores. Todas as películas são obtidas por meio de CSS personalizado.

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interação com o eCatalog Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

O eCatalog Viewer suporta os seguintes gestos de toque que são comuns em outros aplicativos móveis.

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
   <td colname="col2"> <p> Seleciona uma nova miniatura em amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Duplo </p> </td> 
   <td colname="col2"> <p> Aumenta o zoom em um nível até atingir a ampliação máxima. O próximo gesto de toque do duplo redefine o visualizador para o estado de visualização inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Aumenta ou diminui o zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque horizontal ou toque </p> </td> 
   <td colname="col2"> <p> Percorre a lista de páginas de catálogo se uma transição de quadro deslizante for usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque vertical ou clique </p> </td> 
   <td colname="col2"> <p>Quando a imagem está em um estado de redefinição, ela executa uma rolagem de página nativa. </p> <p>Quando as miniaturas estão ativas, rola a lista das miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

É possível ativar um efeito de animação de flip de página realista para navegar entre as páginas do catálogo. Nesses casos, um usuário pode segurar e arrastar um canto da página e virar a página.

Este visualizador também suporta entrada de toque e entrada de mouse em dispositivos Windows com tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

Este visualizador está totalmente acessível ao teclado, conforme descrito em [Acessibilidade e navegação do teclado](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Ferramentas de compartilhamento de mídia social com o eCatalog Viewer {#section-eb575084a99647c3a9591f439f40b412}

O eCatalog Viewer suporta ferramentas de compartilhamento em redes sociais Eles estão disponíveis como um botão na barra de controle principal, que se expande para uma barra de ferramentas de compartilhamento quando um usuário clica ou toca nele.

A barra de ferramentas de compartilhamento contém ícones para cada tipo de canal de compartilhamento suportado, que inclui Facebook, Twitter, compartilhamento de email, compartilhamento de código incorporado e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento incorporado ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou o Twitter é chamado, o visualizador redireciona o usuário para uma caixa de diálogo de compartilhamento padrão de um serviço social. As ferramentas de compartilhamento não estão disponíveis no modo de tela cheia devido às restrições de segurança do navegador da Web.

## Incorporando o eCatalog Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando clicado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador suporta três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação de design responsivo.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação de um dispositivo móvel seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` chamada JavaScript, elemento HTML `A` configurado corretamente ou qualquer outro método adequado.

É recomendável usar uma página HTML predefinida para o modo de operação de pop-up. Nesse caso, ele é chamado [!DNL eCatalogViewer.html] e está localizado na subpasta [!DNL html5/] da implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

A seguir está um exemplo de código HTML que abre o visualizador em uma nova janela:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas uma parte do patrimônio de uma página da web.

Os casos de uso principal são páginas da Web orientadas para desktops ou tablets e também páginas projetadas responsivas que ajustam o layout automaticamente dependendo do tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web que têm um layout estático.

A incorporação de design responsivo supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu container `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu container `DIV`. Se a página da Web definir somente a largura do container `DIV`, deixando sua altura sem restrições, o visualizador escolherá automaticamente sua altura de acordo com a proporção do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à visualização, sem qualquer preenchimento lateral. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas, como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do container do visualizador `DIV`, o visualizador preencherá apenas essa área e seguirá o tamanho que o layout da página da Web fornece. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, na qual a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web, fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o DIV do container.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no cabeçalho HTML. Antes de usar a API do visualizador, certifique-se de incluir [!DNL eCatalogViewer.js]. O arquivo [!DNL eCatalogViewer.js] está localizado na subpasta [!DNL html5/js/] da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores Adobe Dynamic Media Classic e for disponibilizado a partir do mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media Classic com os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>Você só deve fazer referência ao arquivo JavaScript do visualizador principal `include` na sua página. Você não deve fazer referência a nenhum arquivo JavaScript adicional no código da página da Web que possa ser baixado pela lógica do visualizador no tempo de execução. Especificamente, não faça referência direta à biblioteca HTML5 SDK `Utils.js` carregada pelo visualizador do caminho de contexto `/s7viewers` (o chamado SDK consolidado `include`). O motivo é que a localização de `Utils.js` ou bibliotecas semelhantes do visualizador de tempo de execução é totalmente gerenciada pela lógica do visualizador e as alterações de localização entre as versões do visualizador. O Adobe não mantém versões anteriores do visualizador secundário `includes` no servidor.
>
>
>Como resultado, colocar uma referência direta a qualquer JavaScript secundário `include` usado pelo visualizador na página quebrará a funcionalidade do visualizador no futuro quando uma nova versão do produto for implantada.

1. Definindo o DIV do container.

   Adicione um elemento DIV vazio à página onde deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois ela é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a propriedade `position` CSS está definida como `relative` ou `absolute`.

   A seguir está um exemplo de um elemento DIV de espaço reservado definido:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático para o visualizador declarando-o para `.s7ecatalogviewer` classe CSS de nível superior em unidades absolutas ou usando o modificador `stagesize`.

   Você pode colocar o dimensionamento em CSS diretamente na página HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic, ou passado explicitamente usando um comando de estilo.

   Consulte [Personalizando o visualizador do eCatalog](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre como estilizar o visualizador com CSS.

   A seguir está um exemplo de como definir um tamanho de visualizador estático na página HTML:

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Você pode definir o modificador `stagesize` no registro predefinido do visualizador no Dynamic Media Classic, ou passá-lo explicitamente com o código de inicialização do visualizador com a coleção `params`, ou como uma chamada de API conforme descrito na seção Referência de comando, como a seguinte:

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. Inicializando o visualizador.

   Depois de concluir as etapas acima, crie uma instância da classe `s7viewers.eCatalogViewer`, passe todas as informações de configuração para o construtor e chame o método `init()` em uma instância do visualizador. As informações de configuração são passadas ao construtor como um objeto JSON. No mínimo, esse objeto tem o campo `containerId` que contém o nome da ID do container do visualizador e o objeto JSON aninhado `params` com parâmetros de configuração suportados pelo visualizador. Nesse caso, o objeto `params` deve ter pelo menos o URL de disponibilização de imagem transmitido como propriedade `serverUrl` e o ativo inicial como parâmetro `asset`. A API de inicialização baseada em JSON permite que você crie e start o visualizador com uma única linha de código.

   É importante ter o container do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do container por sua ID. Alguns navegadores atrasam a criação de DOM até o final da página da Web. No entanto, para obter compatibilidade máxima, chame o método `init()` imediatamente antes da tag `BODY` de fechamento ou no evento body `onload()`.

   Ao mesmo tempo, o elemento container ainda não deve fazer parte do layout da página da Web. Por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele. Nesse caso, o visualizador atrasa seu processo de inicialização até o momento em que a página da Web traz o elemento de container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   A seguir está um exemplo de criação de uma instância do visualizador, passando as opções mínimas de configuração necessárias para o construtor e chamando o método `init()`. O exemplo supõe que `eCatalogViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `http://s7d1.scene7.com/is/image/` é o URL de disponibilização de imagem e `Viewers/Pluralist` é o ativo:

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o eCatalog Viewer com um tamanho fixo:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporação de design responsivo com altura irrestrita**

Com incorporação de design responsivo, a página da Web normalmente tem algum tipo de layout flexível no lugar que determina o tamanho do tempo de execução do container do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita que o container do visualizador `DIV` pegue 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código HTML da página da Web resultante é semelhante ao seguinte:

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

A adição do visualizador a uma página desse tipo é semelhante à incorporação de tamanho fixo, com a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definindo o DIV do container.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com a incorporação de tamanho fixo. Adicione o container `DIV` ao &quot; detentor&quot; `DIV` existente. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra casos de uso mais reais de incorporação responsiva de design com altura sem restrições:

[Demos ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Incorporação flexível de tamanho com definição de largura e altura**

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ou seja, ele fornece ambos os tamanhos para o &quot; detentor&quot; `DIV` e o centraliza na janela do navegador. Além disso, a página da Web define o tamanho dos elementos `HTML` e `BODY` como 100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com esse construtor de API não aceita parâmetros e parâmetros de configuração são especificados usando os métodos de API `setContainerId()`, `setParam()` e `setAsset()` com chamadas JavaScript separadas.

O exemplo a seguir mostra a incorporação de tamanho fixo à API baseada em setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```

