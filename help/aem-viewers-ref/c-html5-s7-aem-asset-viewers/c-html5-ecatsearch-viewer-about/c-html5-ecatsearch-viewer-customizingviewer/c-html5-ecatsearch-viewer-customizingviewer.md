---
description: Toda personalização visual e a maioria dos comportamentos do Visualizador de pesquisa do catálogo eletrônico são feitos com a criação de um CSS personalizado.
keywords: responsivo
solution: Experience Manager
title: Personalizando o Visualizador de Pesquisa do Catálogo Eletrônico
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---


# Personalizando o Visualizador de Pesquisa do Catálogo Eletrônico{#customizing-ecatalog-search-viewer}

Toda personalização visual e a maioria dos comportamentos do Visualizador de pesquisa do catálogo eletrônico são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para os elementos da interface do usuário.

Uma maneira alternativa de fornecer regras de CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras de CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7ecatalogsearchviewer` ao elemento DOM do contêiner. Se você estiver usando um arquivo CSS externo passado com o comando `style=`, use a classe `.s7ecatalogsearchviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7ecatalogsearchviewer`

## Criando CSS responsivo projetado {#section-c1e74f5114ad418884ca1c95f5ea5b63}

É possível direcionar diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário ou de um layout de página da Web específico. Isso inclui, entre outros, diferentes layouts de página da Web, tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador aceita dois métodos para criar CSS responsivo projetado: Marcadores CSS e consultas de mídia CSS padrão. Você pode usar esses métodos separadamente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador aceita marcadores CSS que possuem classes CSS especiais atribuídas dinamicamente ao elemento do contêiner do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do contêiner do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum `.s7size_large` for usado; se a área estiver próxima em tamanho de um tablet comum, `.s7size_medium` será atribuído. Para áreas semelhantes a telas de celular, `.s7size_small` está definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para diferentes telas e tamanhos de visualizador.

O segundo grupo de marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver recursos de entrada por toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada por toque requer elementos maiores. Caso o dispositivo tenha recursos de entrada e toque do mouse, `.s7touchinput` é definido e o visualizador renderiza uma interface de usuário fácil de tocar.

A amostra de CSS a seguir define o tamanho do botão de zoom em 28 x 28 pixels em sistemas com entrada de mouse e 56 x 56 pixels em dispositivos de toque. Além disso, ele oculta completamente o botão se o tamanho do visualizador se tornar realmente pequeno:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Para direcionar dispositivos com uma densidade de pixels diferente, use consultas de mídia CSS. O seguinte bloco de consulta de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Usar marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo, pois permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, o que pode ser útil para layouts de página projetados responsivos.

Use o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

A detecção de dispositivo também pode ser feita usando queries de mídia CSS puras. Tudo que é delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a visualizadores móveis, use quatro consultas de mídia CSS, definidas em seu CSS na seguinte ordem:

1. Contém apenas regras específicas para todos os dispositivos de toque.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contém apenas regras específicas para tablets com telas de alta resolução.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contém apenas regras específicas para todos os telefones celulares.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contém apenas regras específicas para telefones celulares com telas de alta resolução.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Usando uma abordagem de consultas de mídia, você deve organizar o CSS com detecção de dispositivo da seguinte maneira:

* Primeiro, a seção específica do desktop define todas as propriedades que são específicas do desktop ou comuns a todas as telas.
* E segundo, as quatro consultas de mídia seguem a ordem definida acima e fornecem regras de CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## Sprites CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Muitos elementos da interface do usuário do visualizador são estilizados usando a arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada para o arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Veja a seguir uma amostra de CSS para estilizar um botão de zoom:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

A desvantagem dessa abordagem é que o usuário final apresenta cintilação ou resposta retardada da interface do usuário quando o elemento interagiu pela primeira vez. Essa ação ocorre porque a arte-final da imagem do novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento do número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente, na qual a arte-final de imagem de todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Esse &quot;sprite&quot; tem todos os estados visuais para o determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de como colocar o mesmo botão de zoom acima:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notas e conselhos gerais sobre estilo {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com os elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento de componentes adequados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir propriedades de CSS documentadas neste guia de referência.
* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não no local da página HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie também os ativos padrão ou atualize caminhos no CSS personalizado.
* O formato preferido para a arte-final de bitmap é PNG.
* A arte-final do bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image` .
* As propriedades `width` e `height` de um elemento da interface do usuário definem o tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução como Retina, especifique a arte-final de bitmap duas vezes maior que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` a sua classe CSS.
* Você pode usar vários formatos para o valor de cor que o CSS suporta. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

## Elementos Comuns Da Interface Do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A seguir estão os elementos da interface do usuário que fazem referência à documentação que se aplica ao eCatalog Search Viewer:

* [Botão Adicionar favorito](r-html5-ecatsearch-customize-addfavorite.md)
* [Botão Fechar](r-html5-ecatsearch-customize-closebutton.md)
* [Baixar](r-html5-ecatsearch-customize-download.md)
* [Compartilhamento de email](r-html5-ecatsearch-customize-emailshare.md)
* [Compartilhamento incorporado](r-html5-ecatsearch-customize-embedshare.md)
* [Compartilhamento do Facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Efeito Favoritos](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favoritos](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Exibição de favoritos](r-html5-ecatsearch-customize-favoritesview.md)
* [Botão Primeira página](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Destaque da focagem](r-html5-ecatsearch-customize-focushighlight.md)
* [Botão de tela cheia](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Efeito de ícone](r-html5-ecatsearch-customize-iconeffect.md)
* [Pop-up do painel Informações](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Efeito do mapa de imagem](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Botão Grande da próxima página](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Botão Página anterior grande](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Botão Última página](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Compartilhamento de link](r-html5-ecatsearch-customize-linkshare.md)
* [Barra de controle principal](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Área do visualizador principal](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Botão Próxima página](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicador de página](r-html5-ecatsearch-customize-pageindicator.md)
* [Exibição da página](r-html5-ecatsearch-customize-pageview.md)
* [Botão Página anterior](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Imprimir](r-html5-ecatalog-viewer-20-customize-print.md)
* [Botão Remover favorito](r-html5-ecatsearch-customize-removefavorite.md)
* [Botão Pesquisar](r-html5-ecatsearch-customize-searchbutton.md)
* [Efeito de pesquisa](r-html5-ecatsearch-customize-searcheffect.md)
* [Painel de resultados da pesquisa](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra de controle secundária](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Compartilhamento em redes sociais](r-html5-ecatsearch-customize-socialshare.md)
* [Índice](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniaturas](r-html5-ecatsearch-customize-thumbnails.md)
* [Botão Miniaturas](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Dicas de ferramentas](r-html5-ecatsearch-customize-tooltips.md)
* [Compartilhamento do Twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Botão Exibir todos os favoritos](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Botão Ampliar](r-html5-ecatsearch-customize-zoominbutton.md)
* [Botão Menos zoom](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Botão Redefinir zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)

