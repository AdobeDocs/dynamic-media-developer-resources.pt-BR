---
description: O depurador de vídeo é o controle deslizante horizontal que permite que um usuário procure dinamicamente qualquer posição de tempo no vídeo que está sendo reproduzido.
seo-description: O depurador de vídeo é o controle deslizante horizontal que permite que um usuário procure dinamicamente qualquer posição de tempo no vídeo que está sendo reproduzido.
seo-title: depurador de vídeo
solution: Experience Manager
title: depurador de vídeo
topic: Dynamic Media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---


# depurador de vídeo{#video-scrubber}

O depurador de vídeo é o controle deslizante horizontal que permite que um usuário procure dinamicamente qualquer posição de tempo no vídeo que está sendo reproduzido.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O &#39;botão&#39; do depurador também se move à medida que o vídeo é reproduzido para indicar a posição atual do vídeo durante a reprodução. O depurador de vídeo sempre utiliza toda a largura da barra de controle. É possível esfolar o depurador de vídeo. altere sua altura e posição vertical, por CSS.

A aparência geral do depurador de vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**Propriedades de CSS do depurador de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do depurador de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor do depurador de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os seguintes seletores de classe CSS rastreiam os indicadores de plano de fundo, reprodução e carga:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**Propriedades de CSS da faixa**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da faixa correspondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor da faixa correspondente. </p> </td> 
  </tr> 
 </tbody> 
</table>

O seguinte seletor de classe CSS controla o botão:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**Propriedades de CSS do botão**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento do botão vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Nódulo de arte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O seletor de classe CSS a seguir controla a bolha de tempo reproduzido:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**Propriedades de CSS da bolha de tempo reproduzida**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p> A família de fontes a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p> A cor da fonte a ser usada para o texto de exibição de tempo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da área de bolha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da área de bolha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento da área de bolha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Arte de bolha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento de texto  </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento do texto com a área de bolha. </p> </td> 
  </tr> 
 </tbody> 
</table>

A dica de ferramenta do depurador de vídeo pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

**Exemplo**  - Para configurar um visualizador de vídeo com um depurador de vídeo com cores de rastreamento personalizadas de 10 pixels de altura e posicionado 10 pixels e 35 pixels das bordas superior e esquerda da barra de controle.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Quando a captação de vídeo é ativada com o parâmetro `navigation`, os locais do capítulo são exibidos como marcadores na parte superior da faixa do depurador de vídeo.

O marcador do capítulo de vídeo é controlado pelo seguinte seletor de classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**Propriedades de CSS do marcador de capítulo de vídeo**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do marcador do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do marcador do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Arte-final do marcador do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão. Especificamente, `selected='default'` corresponde ao estado padrão do marcador do capítulo de vídeo e `selected='over'` é usado quando o marcador do capítulo de vídeo é ativado por um gesto de toque ou sobre o mouse.

**Exemplo**  - Para configurar um marcador de capítulo de vídeo com 5 x 8 pixels e que use arte diferente para os estados &quot;padrão&quot; e &quot;sobre&quot;.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

A bolha de capítulo do vídeo é posicionada sobre o marcador de capítulo do vídeo e mostra o título, a hora do start e a descrição de um determinado capítulo. É possível controlar a largura máxima da bolha e o deslocamento vertical em relação à faixa do depurador de vídeo. O restante é calculado automaticamente pelo componente.

A bolha de capítulo do vídeo é controlada pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**Propriedades de CSS da bolha de capítulo do vídeo**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura máxima  </span> </p> </td> 
   <td colname="col2"> <p>Largura máxima da bolha de capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento vertical da faixa do depurador de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar uma bolha de capítulo de vídeo com 235 pixels de largura e oito pixels acima na parte inferior da faixa do depurador de vídeo.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

A bolha de capítulo do vídeo consiste em um cabeçalho e conteúdo opcionais. O cabeçalho tem o tempo de start do capítulo e o título do capítulo opcionais.

O cabeçalho é controlado pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**Propriedades de CSS do cabeçalho da bolha do capítulo do vídeo**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do cabeçalho da bolha do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno para o texto do cabeçalho da bolha do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do cabeçalho da bolha do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha  </span> </p> </td> 
   <td colname="col2"> <p>Altura da linha de texto do cabeçalho da bolha do capítulo do vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar um cabeçalho de bolha de capítulo de vídeo com 22 pixels de altura, uma altura de linha de 22 pixels, uma margem horizontal de 12 pixels e um plano de fundo cinza.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

A hora de start do capítulo de vídeo é controlada pelo seguinte seletor de classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**Propriedades de CSS da hora do start do capítulo do vídeo**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à direita  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento entre a hora do start e o título do capítulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar o tempo de start do capítulo usando a fonte Verdana cinza de dez pixels e tem dez pixels no preenchimento à direita.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

O título do capítulo do vídeo é controlado pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**Propriedades de CSS do título do capítulo do vídeo**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do título do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte do título do capítulo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do título do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do título do capítulo de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar um título de capítulo de vídeo que usa uma fonte Verdana branca, em negrito e dez pixels.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

A descrição do capítulo do vídeo é controlada pelo seguinte seletor de classe CSS:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**Propriedades de CSS da descrição do capítulo do vídeo**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte de descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte da descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes de descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha  </span> </p> </td> 
   <td colname="col2"> <p>Altura da linha de descrição do capítulo do vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno da descrição do capítulo do vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar a descrição do capítulo do vídeo usando uma fonte Verdana cinza escuro, de 11 pixels, com um fundo cinza claro; Altura de linha de 5 pixels, preenchimento horizontal de 12 pixels, preenchimento superior de 12 pixels e preenchimento inferior de 9 pixels.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
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
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**Propriedades de CSS do conector de tecelagem**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda  </span> </p> </td> 
   <td colname="col2"> <p>Cor do conector da borda. </p> <p>Definido como <span class="codeph"> &lt;color&gt; transparente </span> para que somente a cor da borda superior seja definida e as bordas restantes fiquem transparentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura da borda  </span> </p> </td> 
   <td colname="col2"> <p> Largura do conector da borda. </p> <p>Definido como <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> para que a mesma largura seja definida somente para as bordas superior e horizontal e a largura da borda inferior seja <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> Define apenas uma margem inferior negativa. Deve ter o mesmo valor que <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - Para configurar um conector de cunha cinza de seis pixels:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

