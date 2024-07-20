---
title: Amostras interativas
description: O painel de amostras interativas será exibido ao lado do conteúdo do vídeo se os dados interativos tiverem sido passados para o visualizador na configuração. Ele consiste em um banner na parte superior que renderiza texto, como "Clique para exibir", uma coluna de uma ou mais amostras interativas e dois botões de rolagem (disponíveis apenas em sistemas desktop).
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Amostras interativas{#interactive-swatches}

O painel de amostras interativas será exibido ao lado do conteúdo do vídeo se os dados interativos tiverem sido passados para o visualizador na configuração. Ele consiste em um banner na parte superior que renderiza texto, como &quot;Clique para exibir&quot;, uma coluna de uma ou mais amostras interativas e dois botões de rolagem (disponíveis apenas em sistemas desktop).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Em sistemas desktop e em dispositivos de toque, na orientação paisagem, as amostras interativas são renderizadas verticalmente à direita do conteúdo de vídeo. Em dispositivos de toque com orientação de retrato, eles são exibidos na parte inferior do visualizador como uma linha horizontal de amostras.

O seletor de classe CSS a seguir controla o local e a orientação do painel de amostras interativo:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## Propriedades CSS das amostras interativas {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do painel de amostras interativo </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do painel de amostras interativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição superior do painel de amostras interativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição inferior do painel interativo de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição esquerda do painel interativo de amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição direita do painel interativo de amostras. </p> </td> 
  </tr> 
 </tbody> 
</table>

O local e a orientação do tempo de execução do painel de amostras interativo são definidos por uma combinação das propriedades CSS acima, da seguinte maneira:

* Para renderizar as amostras interativas horizontalmente na parte inferior do visualizador, defina a altura como um valor de pixel absoluto; esquerda e inferior como 0px; largura, direita e superior como auto.
* Para renderizar as amostras interativas verticalmente à direita do conteúdo do vídeo, defina a largura como um pixel absoluto; à direita e acima como 0px; à altura, à esquerda e abaixo como auto.

É possível usar marcadores CSS com esse estilo para obter a colocação adaptável do painel de amostras interativo.

## Exemplo {#example}

Para configurar um painel de amostras interativo para renderizar horizontalmente na parte inferior do visualizador em dispositivos de toque na orientação paisagem. E para mostrá-lo verticalmente à direita do conteúdo de vídeo em todos os outros casos:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O tamanho e a posição do banner são gerenciados pelo componente interativo de amostras com base em outro estilo aplicado com CSS e não podem ser definidos explicitamente.

O seletor de classe CSS a seguir controla a aparência do painel de banner:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## Propriedades CSS do painel Banner {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do painel Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto dentro do painel Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda ao redor do painel banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>A espessura da fonte a ser usada para o texto dentro do painel banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>O tamanho da fonte a ser usada para o texto dentro do painel Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>A família da fonte a ser usada para o texto dentro do painel banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>O alinhamento da fonte a ser usada para o texto dentro do painel banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

A dica de ferramenta do banner pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um banner com plano de fundo cinza escuro, borda de dois pixels cinza claro e texto branco centralizado horizontalmente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

O seletor de classe CSS a seguir controla a aparência das amostras:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## Propriedades CSS da área de amostras {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da área de amostras. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-9cadd62a09fd44a280f55ff42437e416}

Para configurar a área de amostras com plano de fundo cinza escuro:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

O seletor de classe CSS a seguir controla o espaçamento entre as miniaturas de amostra:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## Propriedades CSS do espaçamento da miniatura das amostras {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem horizontal e vertical ao redor de cada miniatura. O espaçamento real entre miniaturas é igual à soma das margens esquerda e direita definidas para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-39fb270b7e494a9d99e6e8f6890ec53c}

Para configurar o espaçamento vertical como dez pixels:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

O seletor de classe CSS a seguir controla a aparência de miniaturas individuais:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## Propriedades CSS da aparência de miniaturas individuais {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura oferece suporte ao seletor de atributos `state`, que você pode usar para aplicar capas diferentes a estados de miniatura diferentes. Especificamente, `state="selected"` corresponde à miniatura da imagem atualmente selecionada; `state="default"` corresponde ao restante das miniaturas; `state="over"` é usado ao passar o mouse.

## Exemplo {#section-69fec189ffaa440b97b6b846c320b75b}

Para configurar miniaturas com 100 x 75 pixels:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

O seletor de classe CSS a seguir controla a aparência do rótulo da miniatura:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## Propriedades CSS da aparência do rótulo de miniatura {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-eb141eb6c1154183baa69796edb90536}

Para configurar rótulos para usar branco, alinhado à esquerda, 12 pixels, em fonte Helvetica® e uma borda inferior:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

O seletor de classe CSS a seguir controla a aparência dos botões de rolagem para cima e para baixo:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Não é possível posicionar os botões de rolagem usando as propriedades CSS `top`, `left`, `bottom` e `right`; em vez disso, a lógica do visualizador os posiciona automaticamente.

## Propriedades CSS da aparência dos botões de rolagem para cima e para baixo {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>A posição dentro da imagem do trabalho artístico, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que você pode usar para aplicar capas diferentes aos estados de botão: &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; e &quot; `disabled`&quot;.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

## Exemplo {#section-e6ce4fa084b84288bc7583342b2c510c}

Para configurar um botão de rolagem para cima com 60 x 36 pixels, tenha um trabalho artístico diferente para cada estado e o tire da imagem gráfica do componente:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
