---
title: Depurador de vídeo
description: O depurador de vídeo é o controle deslizante horizontal que permite ao usuário buscar dinamicamente qualquer posição no vídeo em reprodução.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
source-git-commit: 14ca8cd5e1ce60d59806765e573e50417d0ccc50
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Depurador de vídeo{#video-scrubber}

O depurador de vídeo é o controle deslizante horizontal que permite ao usuário buscar dinamicamente qualquer posição no vídeo em reprodução.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O &quot;botão&quot; do depurador também se move conforme o vídeo é reproduzido, para indicar a posição atual do vídeo durante a reprodução. O depurador de vídeo sempre ocupa toda a largura da barra de controle. É possível retirar a capa do depurador de vídeo e alterar sua altura e posição vertical usando CSS.

A aparência geral do depurador de vídeo é controlada com o seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Propriedades CSS do depurador de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do depurador de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do depurador de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os seletores de classe CSS a seguir rastreiam os indicadores de plano de fundo, reprodução e carregamento:

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**Propriedades CSS da faixa**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da faixa correspondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor da faixa correspondente. </p> </td> 
  </tr> 
 </tbody> 
</table>

O seletor de classe CSS a seguir controla o botão:

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**Propriedades CSS do botão**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento vertical do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Obstrução de arte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O seletor de classe CSS a seguir controla a bolha de tempo reproduzida:

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**Propriedades CSS da bolha de tempo reproduzida**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p> A família da fonte a ser usada para o texto de exibição de hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p> A cor da fonte a ser usada para o texto de exibição da hora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da área de bolhas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da área de bolhas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento da área de bolhas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Trabalho artístico em bolha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento do texto com a área da bolha. </p> </td> 
  </tr> 
 </tbody> 
</table>

A dica de ferramenta do depurador de vídeo pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

**Exemplo** - Para configurar um visualizador de vídeo com um depurador de vídeo e cores de faixa personalizadas com dez pixels de altura. Posicione-o a dez pixels e 35 pixels das bordas superior e esquerda da barra de controle.

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Quando o marcador de capítulo de vídeo é ativado com o parâmetro `navigation`, as localizações de capítulo são exibidas como marcadores na parte superior da faixa do depurador de vídeo.

O marcador de capítulo de vídeo é controlado pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**Propriedades CSS do marcador de capítulo de vídeo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do marcador de capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do marcador de capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Arte do marcador de capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que você pode usar para aplicar capas diferentes a estados de botão diferentes. Especificamente, `selected='default'` corresponde ao estado padrão do marcador de capítulo de vídeo e `selected='over'` é usado quando o marcador de capítulo de vídeo é ativado por um gesto de toque ou mouse sobre ele.

**Exemplo** - Para configurar um marcador de capítulo de vídeo com 5 x 8 pixels e usar arte diferente para o estado &quot;padrão&quot; e &quot;acima&quot;.

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

A bolha de capítulo de vídeo é posicionada sobre o marcador de capítulo de vídeo e mostra o título, a hora de início e a descrição de um determinado capítulo. É possível controlar a largura máxima da bolha e o deslocamento vertical em relação à trilha do depurador de vídeo. O restante é calculado automaticamente pelo componente.

A bolha do capítulo de vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**Propriedades CSS da bolha de capítulo de vídeo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura máxima </span> </p> </td> 
   <td colname="col2"> <p>Largura máxima da bolha de capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Deslocamento vertical da trilha do depurador de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar uma bolha de capítulo de vídeo com 235 pixels de largura e oito pixels acima da parte inferior da faixa do depurador de vídeo.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

A bolha do capítulo de vídeo consiste em um cabeçalho e conteúdo opcionais. O cabeçalho tem a hora de início e o título opcionais do capítulo.

O cabeçalho é controlado pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriedades CSS do cabeçalho da bolha do capítulo de vídeo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do cabeçalho de bolha do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno para o texto do cabeçalho de bolha do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do cabeçalho de bolha do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p>Altura da linha de texto do cabeçalho de bolha do capítulo de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar um cabeçalho de bolha de capítulo de vídeo com 22 pixels de altura, uma altura de linha de 22 pixels, uma margem horizontal de 12 pixels e um plano de fundo cinza.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

A hora de início do capítulo de vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Hora de início das propriedades CSS do capítulo de vídeo**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento direito </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento entre a hora de início e o título do capítulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar a hora de início do capítulo usando a fonte Verdana de dez pixels cinza e o preenchimento de dez pixels à direita.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

O título do capítulo de vídeo é controlado pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Propriedades CSS do título do capítulo de vídeo**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do título do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte do título do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do título do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do título do capítulo do vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar um título de capítulo de vídeo que use uma fonte Verdana branca, negrito e de dez pixels.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

A descrição do capítulo de vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**Propriedades CSS da descrição do capítulo de vídeo**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da descrição do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da descrição do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Descrição de capítulo de vídeo espessura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte da descrição do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Descrição de capítulo de vídeo família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p>Altura da linha de descrição do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Descrição do capítulo de vídeo preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar a descrição do capítulo de vídeo usando uma fonte Verdana de 11 pixels cinza escuro, com plano de fundo cinza claro. Uma altura de linha de cinco pixels, preenchimento horizontal de 12 pixels, preenchimento superior de 12 pixels e preenchimento inferior de nove pixels.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

O conector de cunha na parte inferior da bolha de capítulo é controlado pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriedades CSS do conector de cunha**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda </span> </p> </td> 
   <td colname="col2"> <p>Cor do conector da cunha. </p> <p>Definido como <span class="codeph"> &lt;cor&gt; transparente </span>, de modo que somente a cor da borda superior seja definida e as bordas restantes fiquem transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura da borda </span> </p> </td> 
   <td colname="col2"> <p> Largura do conector da cunha. </p> <p>Definido como <span class="codeph"> &lt;largura&gt; &lt;largura&gt; 0 </span> de modo que a mesma largura seja definida somente para as bordas superior e horizontal, e a largura da borda inferior seja <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> Define apenas uma margem inferior negativa. Ele deve ter o mesmo valor que <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - Para configurar um conector de cunha cinza de seis pixels:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
