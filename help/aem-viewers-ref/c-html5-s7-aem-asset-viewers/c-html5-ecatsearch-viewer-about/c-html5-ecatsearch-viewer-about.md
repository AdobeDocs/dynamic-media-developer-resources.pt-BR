---
description: O eCatalog Search Viewer é um visualizador de catálogo que exibe folhetos eletrônicos em um modo espalhado por página ou página por página, o eCatalog permite que os usuários naveguem pelo catálogo usando elementos adicionais da interface do usuário ou o modo de miniaturas dedicado. Os usuários também podem ampliar em cada página para obter mais detalhes.
keywords: responsivo
solution: Experience Manager
title: Pesquisa no catálogo eletrônico
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# Pesquisa no catálogo eletrônico{#ecatalog-search}

O eCatalog Search Viewer é um visualizador de catálogo que exibe folhetos eletrônicos em um modo espalhado por página ou página por página, o eCatalog permite que os usuários naveguem pelo catálogo usando elementos adicionais da interface do usuário ou o modo de miniaturas dedicado. Os usuários também podem ampliar em cada página para obter mais detalhes.

Este visualizador funciona com ecatalogs e oferece suporte a mapas de imagem opcionais e ferramentas de compartilhamento social. Ele tem ferramentas de zoom, ferramentas de navegação em catálogos, suporte em tela cheia, miniaturas e um botão de fechamento opcional. O visualizador também é compatível com ferramentas de compartilhamento social, Imprimir, Download e Favoritos. Ele foi projetado para funcionar em desktops e dispositivos móveis.

O usuário também pode fazer uma pesquisa baseada em palavras-chave ou frases sobre o conteúdo do catálogo.

>[!NOTE]
>
>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador.

Tipo de visualizador 513.

Consulte [Requisitos e pré-requisitos do sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de demonstração {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## Usando o Visualizador de Catálogo Eletrônico {#section-e6c68406ecdc4de781df182bbd8088b4}

O eCatalog Search Viewer representa um arquivo JavaScript principal e um conjunto de arquivos auxiliares (uma única inclusão do JavaScript com todos os componentes do SDK do visualizador usados por esse visualizador específico, ativos, CSS) baixados pelo visualizador em tempo de execução

Você pode usar o Visualizador de pesquisa do eCatalog no modo pop-up usando uma página de HTML pronta para produção fornecida com IS-Viewers ou no modo incorporado, onde ele é integrado na página da Web de destino usando a API documentada.

A configuração e o esfolamento são semelhantes aos dos outros visualizadores. Todo o esfolamento é obtido por meio de CSS personalizado.

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagir com o Visualizador de Pesquisa do Catálogo Eletrônico {#section-642e66ca38cd4032992840ec6c0b0cd2}

O eCatalog Search Viewer oferece suporte aos seguintes gestos de toque que são comuns em outros aplicativos móveis.

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
   <td colname="col1"> <p>Toque duplo </p> </td> 
   <td colname="col2"> <p> Aumenta o zoom em um nível até atingir a ampliação máxima. O próximo gesto de toque duplo redefine o visualizador para o estado de visualização inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinça </p> </td> 
   <td colname="col2"> <p>Aumenta ou diminui o zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toque ou cintilação horizontal </p> </td> 
   <td colname="col2"> <p>Rola pela lista de páginas de catálogo se uma transição de quadro de slide for usada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Passar ou piscar na vertical </p> </td> 
   <td colname="col2"> <p>Quando a imagem está em um estado de redefinição, ela executa uma rolagem de página nativa. </p> <p>Quando as miniaturas estão ativas, elas rolam a lista de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

É possível ativar um efeito de animação de flip de página realista para navegar entre as páginas de catálogo. Nesses casos, um usuário pode segurar e arrastar um canto de página e virar a página.

Este visualizador também suporta entrada de toque e entrada de mouse em dispositivos Windows com uma tela sensível ao toque e mouse. No entanto, esse suporte é limitado somente aos navegadores da Web Chrome, Internet Explorer 11 e Edge.

## Ferramentas de compartilhamento em redes sociais com o Visualizador de pesquisa do catálogo eletrônico {#section-eb575084a99647c3a9591f439f40b412}

O eCatalog Search Viewer oferece suporte a ferramentas de compartilhamento em redes sociais Eles estão disponíveis como um botão na barra de controle principal, que se expande em uma barra de ferramentas de compartilhamento quando um usuário clica ou toca nela.

A barra de ferramentas de compartilhamento contém ícones para cada tipo de canal de compartilhamento compatível, que inclui Facebook, Twitter, compartilhamento de email, compartilhamento de código de incorporação e compartilhamento de link. Quando as ferramentas de compartilhamento de email, compartilhamento de incorporação ou compartilhamento de link são ativadas, o visualizador exibe uma caixa de diálogo modal com um formulário de entrada de dados correspondente. Quando o Facebook ou Twitter é chamado, o visualizador redireciona o usuário para um diálogo de compartilhamento padrão a partir de um serviço social. O compartilhamento de ferramentas não está disponível no modo de tela cheia devido a restrições de segurança do navegador da Web.

O recurso Pesquisa do visualizador está disponível como um ícone de vidro na barra de ferramentas principal. Clicar ou tocar no ícone ativa o painel Pesquisar com um campo de entrada. Depois de inserir uma palavra-chave ou frase e pressionar Enter, o visualizador renderiza os resultados da pesquisa no painel e realça as palavras encontradas na exibição principal.

## Incorporando o visualizador de pesquisa do catálogo eletrônico {#section-6bb5d3c502544ad18a58eafe12a13435}

Páginas da Web diferentes têm necessidades diferentes para o comportamento do visualizador. Às vezes, uma página da Web fornece um link que, quando selecionado, abre o visualizador em uma janela separada do navegador. Em outros casos, é necessário incorporar o visualizador diretamente na página de hospedagem. No último caso, a página da Web pode ter um layout de página estático ou usar um design responsivo que é exibido de forma diferente em dispositivos diferentes ou para tamanhos de janela de navegador diferentes. Para acomodar essas necessidades, o visualizador aceita três modos de operação principais: pop-up, incorporação de tamanho fixo e incorporação responsiva de design.

**Sobre o modo pop-up**

No modo pop-up, o visualizador é aberto em uma janela ou guia separada do navegador da Web. Pega toda a área da janela do navegador e se ajusta caso o navegador seja redimensionado ou a orientação de um dispositivo móvel seja alterada.

O modo pop-up é o mais comum para dispositivos móveis. A página da Web carrega o visualizador usando `window.open()` Chamada de JavaScript, configurada corretamente `A` HTML ou qualquer outro método adequado.

É recomendável usar uma página de HTML pronta para uso no modo de operação pop-up. Nesse caso, é chamado de [!DNL eCatalogSearchViewer.html] e está localizado dentro do [!DNL html5/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Você pode obter personalização visual aplicando CSS personalizado.

Este é um exemplo de código HTML que abre o visualizador em uma nova janela:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Sobre o modo de incorporação de tamanho fixo e o modo de incorporação de design responsivo**

No modo incorporado, o visualizador é adicionado à página da Web existente, que pode já ter algum conteúdo de cliente não relacionado ao visualizador. O visualizador normalmente ocupa apenas parte do imóvel de uma página da web.

Os casos de uso principais são páginas da Web orientadas para desktops ou tablets, além de páginas projetadas responsivas que ajustam o layout automaticamente de acordo com o tipo de dispositivo.

A incorporação de tamanho fixo é usada quando o visualizador não altera seu tamanho após o carregamento inicial. Essa é a melhor opção para páginas da Web com layout estático.

A incorporação responsiva de design supõe que o visualizador talvez precise ser redimensionado no tempo de execução em resposta à alteração de tamanho de seu contêiner `DIV`. O caso de uso mais comum é adicionar um visualizador a uma página da Web que use um layout de página flexível.

No modo de incorporação de design responsivo, o visualizador se comporta de forma diferente dependendo da maneira como a página da Web dimensiona seu contêiner `DIV`. Se a página da Web definir somente a largura do contêiner `DIV`, deixando sua altura sem restrições, o visualizador escolhe automaticamente sua altura de acordo com a proporção de aspecto do ativo usado. Essa funcionalidade garante que o ativo se ajuste perfeitamente à exibição sem qualquer preenchimento nas laterais. Esse caso de uso é o mais comum para páginas da Web que usam estruturas de layout responsivas como Bootstrap, Foundation e assim por diante.

Caso contrário, se a página da Web definir a largura e a altura do contêiner do visualizador `DIV`, o visualizador preenche apenas essa área e segue o tamanho fornecido pelo layout da página da Web. Um bom exemplo é incorporar o visualizador em uma sobreposição modal, onde a sobreposição é dimensionada de acordo com o tamanho da janela do navegador da Web.

**Incorporação de tamanho fixo**

Você adiciona o visualizador a uma página da Web fazendo o seguinte:

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Definição do tamanho do visualizador.
1. Criação e inicialização do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.

   A criação de um visualizador requer a adição de uma tag de script no HTML head. Antes de usar a API do visualizador, verifique se você incluiu [!DNL eCatalogSearchViewer.js]. O [!DNL eCatalogSearchViewer.js] O arquivo está localizado sob a variável [!DNL html5/js/] subpasta da sua implantação padrão do IS-Viewers:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Você pode usar um caminho relativo se o visualizador for implantado em um dos servidores do Adobe Dynamic Media e ele for exibido no mesmo domínio. Caso contrário, especifique um caminho completo para um dos servidores Adobe Dynamic Media que têm os IS-Viewers instalados.

O caminho relativo tem a seguinte aparência:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Definição do DIV do contêiner.

   Adicione um elemento DIV vazio à página onde você deseja que o visualizador apareça. O elemento DIV deve ter sua ID definida, pois essa ID é passada posteriormente para a API do visualizador.

   O espaço reservado DIV é um elemento posicionado, o que significa que a variável `position` A propriedade CSS está definida como `relative` ou `absolute`.

   Este é um exemplo de um elemento DIV de espaço reservado definido:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Definição do tamanho do visualizador

   Você pode definir o tamanho estático do visualizador declarando-o para `.s7ecatalogsearchviewer` classe CSS de nível superior em unidades absolutas ou usando `stagesize` modificador.

   Você pode colocar o dimensionamento no CSS diretamente na página do HTML ou em um arquivo CSS do visualizador personalizado, que é posteriormente atribuído a um registro predefinido do visualizador no Dynamic Media Classic, ou passado explicitamente usando um comando style.

   Consulte [Personalizar o visualizador de catálogo eletrônico](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) para obter mais informações sobre o estilo do visualizador com CSS.

   Este é um exemplo de definição de um tamanho de visualizador estático em HTML page:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   É possível definir a variável `stagesize` modificador no registro predefinido do visualizador no Dynamic Media Classic ou passe-o explicitamente com o código de inicialização do visualizador com `params` ou como uma chamada de API, conforme descrito na seção Referência de comando , como o seguinte:

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Inicializando o visualizador.

   Depois de concluir as etapas acima, crie uma instância de `s7viewers.eCatalogSearchViewer` classe , passe todas as informações de configuração para seu construtor e chame `init()` em uma instância do visualizador. As informações de configuração são passadas para o construtor como um objeto JSON. No mínimo, esse objeto tem a variável `containerId` campo que contém o nome da ID do contêiner do visualizador e aninhado `params` Objeto JSON com parâmetros de configuração compatíveis com o visualizador. Nesse caso, a variável `params` O objeto deve ter pelo menos o URL de disponibilização de imagens passado como `serverUrl` e o ativo inicial como `asset` parâmetro. A API de inicialização baseada em JSON permite criar e iniciar o visualizador com uma única linha de código.

   É importante ter o contêiner do visualizador adicionado ao DOM para que o código do visualizador possa encontrar o elemento do contêiner por sua ID. Alguns navegadores atrasam a criação de DOM até o fim da página da Web. No entanto, para ter compatibilidade máxima, chame a função `init()` método antes de fechar `BODY` ou no corpo `onload()` evento.

   Ao mesmo tempo, o elemento de contêiner ainda não deve fazer parte do layout da página da Web. Por exemplo, pode estar oculto usando `display:none` estilo atribuído a ele. Nesse caso, o visualizador atrasa o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

   Este é um exemplo de criação de uma instância do visualizador, transmitindo as opções mínimas necessárias de configuração ao construtor e chamando a função `init()` método . O exemplo assume `eCatalogSearchViewer` é a instância do visualizador; `s7viewer` é o nome do espaço reservado `DIV`; `https://s7d1.scene7.com/is/image/` é o URL de disponibilização de imagens e `Viewers/Pluralist` é o ativo:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   O código a seguir é um exemplo completo de uma página trivial da Web que incorpora o Visualizador de pesquisa do catálogo eletrônico com um tamanho fixo:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporação de design responsivo com altura irrestrita**

Com a incorporação responsiva do design, a página da Web normalmente tem algum tipo de layout flexível em vigor que determina o tamanho de tempo de execução do contêiner do visualizador `DIV`. Para fins deste exemplo, suponha que a página da Web permita o contêiner do visualizador `DIV` para obter 40% do tamanho da janela do navegador da Web, deixando sua altura sem restrições. O código de HTML da página da Web resultante é semelhante ao seguinte:

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

Adicionar o visualizador a essa página é semelhante à incorporação de tamanho fixo, com a única diferença é que você não precisa definir explicitamente o tamanho do visualizador.

1. Adicionar o arquivo JavaScript do visualizador à sua página da Web.
1. Definição do DIV do contêiner.
1. Criação e inicialização do visualizador.

Todas as etapas acima são as mesmas que com incorporação de tamanho fixo. Adicionar o contêiner `DIV` ao atual &quot;detentor&quot; `DIV`. O código a seguir é um exemplo completo. Você pode ver como o tamanho do visualizador muda quando o navegador é redimensionado e como a proporção do visualizador corresponde ao ativo.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

A página de exemplos a seguir ilustra casos de uso mais reais da incorporação responsiva de design com altura irrestrita:

[Demonstrações ao vivo](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Incorporação flexível de tamanho com largura e altura definidas**

No caso de incorporação de tamanho flexível com largura e altura definidas, o estilo da página da Web é diferente. Ou seja, fornece ambos os tamanhos ao &quot;detentor&quot; `DIV` e centraliza na janela do navegador. Além disso, a página da Web define o tamanho da variável `HTML` e `BODY` para 100%:

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

As etapas de incorporação restantes são idênticas à incorporação responsiva de design com altura irrestrita. O exemplo resultante é o seguinte:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Como incorporar usando a API baseada em setter**

Em vez de usar a inicialização baseada em JSON, é possível usar a API baseada em setter e o construtor no-args. Com esse construtor de API não utiliza parâmetros e os parâmetros de configuração são especificados usando `setContainerId()`, `setParam()`e `setAsset()` Métodos de API com chamadas JavaScript separadas.

O exemplo a seguir mostra a incorporação de tamanho fixo com a API baseada em setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
