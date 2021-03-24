---
description: O painel Chamar para ação é exibido quando o vídeo termina e exibe todas as amostras interativas associadas ao vídeo em particular.
solution: Experience Manager
title: Chamada à ação
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 0%

---


# Chame para ação{#call-to-action}

O painel Chamar para ação é exibido quando o vídeo termina e exibe todas as amostras interativas associadas ao vídeo em particular.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O painel consiste em uma área de cabeçalho que mostra o título do vídeo, um botão de reprodução no canto superior direito e amostras interativas reais mostradas como uma grade rolável. Você pode desativar o painel usando o atributo de configuração [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6).

A chamada para o painel de ação sempre ocupa toda a área disponível do visualizador.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

O seguinte seletor de classe CSS controla a aparência da cor do fundo no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction
```

## Propriedades CSS da cor de fundo da chamada para o painel de ação {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo da chamada para o painel de ação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example}

Para configurar uma chamada para o painel de ação com fundo cinza escuro:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

O seguinte seletor de classe CSS controla a aparência do cabeçalho no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## Propriedades CSS da chamada para o cabeçalho do painel de ação {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo do cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Borda inferior do cabeçalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-1}

Para configurar um cabeçalho com 70 pixels de altura, com um plano de fundo cinza escuro e uma borda cinza ligeiramente mais clara de dois pixels ao longo da parte inferior:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

O seguinte seletor de classe CSS controla a aparência do título do cabeçalho no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## Propriedades CSS do título do cabeçalho no painel de ação chamada para :  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto dentro do banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha  </span> </p> </td> 
   <td colname="col2"> <p>Altura da linha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p> Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento de texto  </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento do texto no banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à esquerda  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento esquerdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à direita  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento direito para permitir espaço para o botão Reproduzir . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-2}

Para configurar um título de vídeo com uma altura de linha de 70 pixels, tamanho de fonte de 25 pixels, cor branca e alinhamento à esquerda:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

O seguinte seletor de classe CSS controla a aparência do botão fechar no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## Propriedades de CSS do botão Fechar no painel de ação da chamada para : {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição da parte superior do cabeçalho, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição à direita do cabeçalho, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

## Exemplo {#example-3}

Para configurar um botão de repetição com 28 x 28 pixels; posicionados 20 pixels a partir da parte superior e da extremidade direita do cabeçalho; exibe uma imagem diferente para cada um dos quatro estados de botão diferentes; obtém a arte-final da imagem do componente:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

O seguinte seletor de classe CSS controla a aparência da exibição de grade de miniatura no painel de ação chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## Propriedades CSS da exibição de grade de miniatura no painel de ação chamada para :  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-4}

Para configurar uma área de miniaturas com um fundo cinza escuro:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

O seguinte seletor de classe CSS controla a aparência da célula de polegar no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## Propriedades de CSS da célula de miniatura no painel de ação da chamada para : {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> Tamanho da margem horizontal e vertical ao redor de cada miniatura. </p> <p>O espaçamento horizontal real da miniatura é igual à soma da margem esquerda e direita definida para <span class="codeph"> .s7thumbcell </span>. A mesma regra também se aplica, mas ao espaçamento vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-5}

Para configurar o espaçamento horizontal de 24 pixels e o espaçamento vertical de 18 pixels:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

O seguinte seletor de classe CSS controla a aparência da miniatura no painel de ação da chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## Propriedades de CSS da miniatura no painel de ação da chamada para : {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura é compatível com o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Em particular, `state="selected"` corresponde à miniatura da imagem atualmente selecionada; `state="default"` corresponde ao resto das miniaturas; `state="over"` é usado com o mouse.

## Exemplo {#example-6}

Para configurar miniaturas com 94 x 100 pixels:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

O seguinte seletor de classe CSS controla a aparência do rótulo de miniatura no painel de ação chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## Propriedades CSS do rótulo da miniatura no painel de ação da chamada para : {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento de texto  </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento horizontal do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-7}

Para configurar rótulos que usam uma cor branca, seja alinhado no centro a 15 pixels e use uma fonte Arial:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Se houver mais miniaturas do que podem caber verticalmente na exibição, elas renderizarão uma barra de rolagem vertical no lado direito. Por padrão, a chamada para o painel de ação renderiza uma pequena barra vertical sem botões de polegar e rolagem. No entanto, é possível personalizar a barra alterando o CSS do visualizador.

O seguinte seletor de classe CSS controla a aparência da área da barra de rolagem no painel de ação chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## Propriedades de CSS da área da barra de rolagem no painel de ação chamada: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p> Largura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento da barra de rolagem vertical na parte superior da área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento da barra de rolagem vertical na parte inferior da área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Deslocamento da barra de rolagem horizontal na borda direita da área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-8}

Para configurar uma barra de rolagem com largura de 22 pixels e que não tenha margem da parte superior, direita ou inferior da área de miniaturas:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

O rastreamento da barra de rolagem é a área entre os botões da barra de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa.

O seguinte seletor de classe CSS controla a aparência do rastreamento da barra de rolagem no painel de ação chamada para :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## Propriedades CSS da barra de rolagem da faixa {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da barra de rolagem da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da barra de faixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-9}

Para configurar um rastreamento de barra de rolagem com 22 pixels de largura e uma cor cinza:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

O polegar da barra de rolagem se move verticalmente na área de trilha de rolagem. A sua posição vertical é totalmente controlada pela lógica do componente; no entanto, a altura do polegar não muda dinamicamente, dependendo da quantidade de conteúdo.

O seguinte seletor de classe CSS controla a aparência da altura do polegar e de outros aspectos:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## Propriedades CSS da altura do polegar no painel de ação: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento vertical entre a parte superior da via. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento vertical entre a parte inferior da via. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Imagem exibida para um determinado estado de polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas aos seguintes estados de miniatura diferentes: `"up"`, `"down"`, `"over"` e `"disabled"`.

## Exemplo {#example-10}

Para configurar um polegar da barra de rolagem com 6 x 167 pixels, ele possui três cantos arredondados de pixels e uma cor cinza:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

O seguinte seletor de classe CSS controla a aparência dos botões de rolagem superior e inferior:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Não é possível posicionar botões de rolagem usando propriedades CSS superior, esquerda, inferior ou direita; a lógica do visualizador os posiciona automaticamente. A chamada para o painel de ação no visualizador de vídeo interativo não usa esses botões na barra de rolagem, então seu tamanho é definido como 0 pixels no CSS padrão.

## Propriedades CSS dos botões de rolagem superior e inferior no painel de ação da chamada para:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p> Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esses botões suportam o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes aos seguintes estados de miniatura diferentes: `"up"`, `"down"`, `"over"` e `"disabled"`.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Exemplo {#example-11}

Desative os botões de rolagem definindo seu tamanho como 0 e ocultando-os:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

