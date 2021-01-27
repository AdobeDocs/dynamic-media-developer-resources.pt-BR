---
description: Toda personalização visual e a maioria dos comportamentos do visualizador de pesquisa do eCatalog são feitos por meio da criação de um CSS personalizado.
keywords: responsive
seo-description: Toda personalização visual e a maioria dos comportamentos do visualizador de pesquisa do eCatalog são feitos por meio da criação de um CSS personalizado.
seo-title: Personalização do eCatalog Search Viewer
solution: Experience Manager
title: Personalização do eCatalog Search Viewer
topic: Dynamic Media
uuid: a715399b-7b02-4656-8257-4c390c6f629c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 0%

---


# Personalização do eCatalog Search Viewer{#customizing-ecatalog-search-viewer}

Toda personalização visual e a maioria dos comportamentos do visualizador de pesquisa do eCatalog são feitos por meio da criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão para o visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para os elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7ecatalogsearchviewer` ao elemento DOM do container. Se você estiver usando um arquivo CSS externo transmitido com o comando `style=`, use a classe `.s7ecatalogsearchviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifice adicionalmente este seletor com uma ID do elemento DOM do container da seguinte maneira:

`#<containerId>.s7ecatalogsearchviewer`

## Criação de CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63} projetado responsivo

É possível público alvo de diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que seu conteúdo seja exibido de forma diferente, dependendo do dispositivo do usuário ou de um layout de página da Web específico. Isso inclui, mas não se limita a, diferentes layouts de página da Web, tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador suporta dois métodos para criar CSS responsivo projetado: Marcadores CSS e query de mídia CSS padrão. É possível usar esses métodos independentemente ou em conjunto.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador oferece suporte a marcadores CSS que classes CSS especiais atribuídas dinamicamente ao elemento de container do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do container do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de área de trabalho comum `.s7size_large` for usada; se a área estiver próxima em tamanho a um tablet comum `.s7size_medium` for atribuída. Para áreas semelhantes a telas de telefone móvel `.s7size_small` está definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver capacidades de entrada de toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada de toque requer elementos maiores. Se o dispositivo tiver recursos de entrada e toque do mouse, `.s7touchinput` será definido e o visualizador renderizará uma interface de usuário fácil de tocar.

A amostra de CSS a seguir define o tamanho do botão para 28 x 28 pixels em sistemas com entrada do mouse e 56 x 56 pixels em dispositivos de toque. Além disso, oculta completamente o botão se o tamanho do visualizador se tornar realmente pequeno:

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

Para público alvo de dispositivos com uma densidade de pixels diferente, use query de mídia CSS. O seguinte bloco de query de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar um CSS responsivo projetado, pois permite público alvo não apenas do tamanho da tela do dispositivo, mas do tamanho real do visualizador, o que pode ser útil para layouts de página com design responsivo.

Use o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Query de mídia CSS**

A detecção de dispositivos também pode ser feita usando query de mídia CSS. Tudo o que está incluído em um determinado bloco de query de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado aos Visualizadores móveis, use quatro query de mídia CSS, definidos no CSS na seguinte ordem:

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

Usando uma abordagem de query de mídia, você deve organizar o CSS com detecção de dispositivos da seguinte maneira:

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* Em segundo lugar, os quatro query de mídia seguem a ordem definida acima e fornecem regras de CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicado do CSS do visualizador inteiro em cada query de mídia. Somente as propriedades específicas a determinados dispositivos são redefinidas em um query de mídia.

## Sprites CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Muitos elementos da interface do usuário do visualizador têm estilo usando arte-final bitmap e mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte-final de bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada ao arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. A seguir está um exemplo de CSS para estilizar um botão de zoom:

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

A desvantagem dessa abordagem é que o usuário final sofre oscilações ou retardamento da resposta da interface do usuário quando o elemento é interagido pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento no número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente na qual a arte-final de imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Tal &quot;sprite&quot; tem todos os estados visuais para um determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de como estilizar o mesmo botão de zoom de acima:

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

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento dos componentes apropriados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de referência.
* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não ao local da página HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie também os ativos padrão ou atualize os caminhos no CSS personalizado.
* O formato preferido para a arte-final bitmap é PNG.
* A arte-final bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image`.
* As propriedades `width` e `height` de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução, como Retina, especifique a arte-final bitmap duas vezes maior que o tamanho do elemento lógico da interface do usuário. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à sua classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você pode usar o formato `#RRGGBB`.

## Elementos Comuns da Interface do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A seguir estão os elementos da interface do usuário que fazem referência à documentação que se aplica ao eCatalog Search Viewer:

* [Botão Adicionar favorito](r-html5-ecatsearch-customize-addfavorite.md)
* [Botão Fechar](r-html5-ecatsearch-customize-closebutton.md)
* [Download](r-html5-ecatsearch-customize-download.md)
* [Compartilhamento de email](r-html5-ecatsearch-customize-emailshare.md)
* [Compartilhamento incorporado](r-html5-ecatsearch-customize-embedshare.md)
* [Compartilhamento no Facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Efeito Favoritos](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favoritos](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Visualização Favoritos](r-html5-ecatsearch-customize-favoritesview.md)
* [Botão Primeira página](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Destaque do foco](r-html5-ecatsearch-customize-focushighlight.md)
* [Botão de tela cheia](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Efeito Ícone](r-html5-ecatsearch-customize-iconeffect.md)
* [Pop-up do painel Informações](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Efeito Mapa de imagem](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Botão Grande Próxima Página](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Botão Página anterior grande](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Botão Última página](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Compartilhamento de links](r-html5-ecatsearch-customize-linkshare.md)
* [Barra de controle principal](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Área do visualizador principal](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Botão Próxima página](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicador de página](r-html5-ecatsearch-customize-pageindicator.md)
* [Visualização da página](r-html5-ecatsearch-customize-pageview.md)
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
* [Compartilhamento no Twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Botão visualização de todos os favoritos](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Botão Mais zoom](r-html5-ecatsearch-customize-zoominbutton.md)
* [Botão Menos zoom](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Botão Redefinir zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)

