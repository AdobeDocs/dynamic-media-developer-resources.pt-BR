---
title: Personalização do Visualizador de pesquisa do eCatalog
description: Toda a personalização visual e a maioria das personalizações de comportamento do eCatalog Search Viewer são feitas criando um CSS personalizado.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# Personalização do Visualizador de pesquisa do eCatalog{#customizing-ecatalog-search-viewer}

Toda a personalização visual e a maioria das personalizações de comportamento do eCatalog Search Viewer são feitas criando um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no `style=` comando.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que o padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornecerá estilos padrão internos para os elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui `.s7ecatalogsearchviewer` ao elemento DOM do contêiner. Se você estiver usando um arquivo CSS externo passado com o `style=` comando, use `.s7ecatalogsearchviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, também deverá qualificar esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7ecatalogsearchviewer`

## Criação de CSS responsivo projetado {#section-c1e74f5114ad418884ca1c95f5ea5b63}

É possível direcionar diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário ou de um layout de página da Web específico. Esse direcionamento inclui, mas não está limitado a, diferentes layouts de página da Web, tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador suporta dois métodos para criar CSS responsivo projetado: marcadores CSS e consultas de mídia CSS padrão. Você pode usar esses métodos independentemente ou juntos.

**Marcadores CSS**

Para criar CSS responsivo projetado, o visualizador suporta marcadores CSS que classes CSS especiais dinamicamente atribuídas ao elemento de contêiner do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium`, e `.s7size_small` classes. Elas são aplicadas com base na área de tempo de execução do container do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum `.s7size_large` é usada; se a área estiver próxima em tamanho de um dispositivo de tablet comum `.s7size_medium` é atribuído. Para áreas semelhantes a telas de telefones celulares. O marcador `.s7size_small` está definido. O principal objetivo desses marcadores CSS é criar diferentes layouts de interface de usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de Marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. O marcador `.s7touchinput` é definido se o dispositivo atual tiver recursos de entrada de toque; caso contrário, `.s7mouseinput` é usada. Esses marcadores têm como objetivo criar elementos de entrada da interface do usuário com diferentes tamanhos de tela para diferentes tipos de entrada, pois normalmente a entrada por toque requer elementos maiores. Caso o dispositivo tenha recursos de entrada do mouse e de toque, `.s7touchinput` estiver definido e o visualizador renderizar uma interface do usuário amigável para toque.

O exemplo de CSS a seguir define o tamanho do botão de zoom de aproximação para 28 x 28 pixels em sistemas com entrada de mouse e 56 x 56 pixels em dispositivos de toque. Além disso, ele oculta completamente o botão se o tamanho do visualizador se tornar muito pequeno:

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

Para direcionar dispositivos com uma densidade de pixels diferente, use as consultas de mídia CSS. O seguinte bloco de consulta de mídia conteria CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo. Ela permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, útil para layouts de página com design responsivo.

Use o arquivo CSS do visualizador padrão como um exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

A detecção de dispositivos também pode ser feita usando consultas de mídia CSS pura. Tudo o que está delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a Visualizadores móveis, use quatro consultas de mídia CSS, definidas em seu CSS na seguinte ordem:

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

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* E, em segundo lugar, as quatro consultas de mídia vão na ordem definida acima e fornecem regras CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## Sprites CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Muitos elementos da interface do usuário do visualizador são estilizados usando arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: &quot;up&quot;, &quot;over&quot; e &quot;down&quot;. Cada estado exige que seu próprio trabalho artístico de bitmap seja atribuído.

Com uma abordagem clássica de estilo, o CSS teria uma referência separada a um arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Este é um exemplo de CSS para criar o estilo de um botão de zoom:

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

A desvantagem dessa abordagem é que o usuário final apresenta oscilação ou atraso na resposta da interface do usuário quando o elemento recebe interação pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um pequeno impacto negativo no desempenho devido a um aumento no número de chamadas HTTP para o servidor.

Sprites CSS é uma abordagem diferente, onde a arte-final da imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Essa &quot;imagem&quot; tem todos os estados visuais para o elemento fornecido posicionados um após o outro. Ao estilizar um elemento de interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a variável `background-position` A propriedade é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o empilham verticalmente. Abaixo está um exemplo &quot;sprite&quot; com o estilo do mesmo botão de zoom de cima:

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

## Observações gerais sobre o estilo e conselhos {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso do `!IMPORTANT` a regra não tem suporte para elementos do visualizador de estilos. Em especial, `!IMPORTANT` A regra não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. O motivo é que isso pode afetar o comportamento dos componentes corretos. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de referência.
* Todos os caminhos para ativos externos no CSS são resolvidos em relação ao local do CSS, não ao local da página do HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie os ativos padrão ou atualize os caminhos no CSS personalizado.
* O formato preferido para arte-final de bitmap é PNG.
* O trabalho artístico de bitmap é atribuído a elementos da interface do usuário usando o `background-image` propriedade.
* A variável `width` e `height` as propriedades de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução como o Retina, especifique um trabalho artístico de bitmap duas vezes maior do que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique o `-webkit-background-size:contain` para dimensionar o plano de fundo até o tamanho do elemento da interface lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à sua classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

## Elementos comuns da interface do usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao eCatalog Search Viewer:

* [Botão Adicionar favorito](r-html5-ecatsearch-customize-addfavorite.md)
* [Botão Fechar](r-html5-ecatsearch-customize-closebutton.md)
* [Baixar](r-html5-ecatsearch-customize-download.md)
* [Compartilhamento de email](r-html5-ecatsearch-customize-emailshare.md)
* [Incorporar compartilhamento](r-html5-ecatsearch-customize-embedshare.md)
* [Compartilhamento facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Efeito Favoritos](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Favoritos](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Exibição de favoritos](r-html5-ecatsearch-customize-favoritesview.md)
* [Botão Primeira página](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Foco em destaque](r-html5-ecatsearch-customize-focushighlight.md)
* [botão de tela cheia](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Efeito do ícone](r-html5-ecatsearch-customize-iconeffect.md)
* [Pop-up do painel Informações](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Efeito do mapa de imagem](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Botão grande da próxima página](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Botão grande da página anterior](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Botão Última página](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Compartilhamento de link](r-html5-ecatsearch-customize-linkshare.md)
* [Barra de controle principal](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Área do visualizador principal](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Botão Próxima página](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicador de página](r-html5-ecatsearch-customize-pageindicator.md)
* [Exibição de página](r-html5-ecatsearch-customize-pageview.md)
* [Botão da página anterior](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Imprimir](r-html5-ecatsearch-customize-print.md)
* [Botão Remover Favorito](r-html5-ecatsearch-customize-removefavorite.md)
* [Botão Pesquisar](r-html5-ecatsearch-customize-searchbutton.md)
* [Efeito de pesquisa](r-html5-ecatsearch-customize-searcheffect.md)
* [Painel de resultados da pesquisa](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra de controle secundária](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Compartilhamento social](r-html5-ecatsearch-customize-socialshare.md)
* [Índice](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniaturas](r-html5-ecatsearch-customize-thumbnails.md)
* [Botão Miniaturas](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Dicas de ferramenta](r-html5-ecatsearch-customize-tooltips.md)
* [Compartilhamento de twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Botão Exibir todos os favoritos](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Botão de Mais zoom](r-html5-ecatsearch-customize-zoominbutton.md)
* [Botão de menos zoom](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Botão de redefinição de zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
