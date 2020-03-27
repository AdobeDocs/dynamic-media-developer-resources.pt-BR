---
description: O controle de volume silencioso é exibido inicialmente como um botão que permite ao usuário silenciar ou ativar o som do player de vídeo.
seo-description: O controle de volume silencioso é exibido inicialmente como um botão que permite ao usuário silenciar ou ativar o som do player de vídeo.
seo-title: Volume mutável
solution: Experience Manager
title: Volume mutável
topic: Dynamic media
uuid: d7eafff8-dd98-42e2-9d45-e291fe372d8c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Volume mutável{#mutable-volume}

O controle de volume silencioso é exibido inicialmente como um botão que permite ao usuário silenciar ou ativar o som do player de vídeo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Quando um usuário passa o mouse sobre o botão, um controle deslizante é exibido, permitindo que o usuário defina o volume. O controle de volume silencioso pode ser dimensionado, esfolado e posicionado, em relação à barra de controle que o contém, por CSS.

A aparência da área de volume mutável é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7mutablevolume
```

**Propriedades de CSS do volume mutável**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda superior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda direita, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do controle de volume mutável. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do controle de volume mutável. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> A cor do controle de volume mutável. </p> </td> 
  </tr> 
 </tbody> 
</table>

A aparência do botão silenciar/ativar é controlada pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

É possível controlar a imagem de plano de fundo para cada estado de botão. O tamanho do botão é herdado do tamanho do controle de volume.

**Propriedades de CSS da imagem do botão**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta os seletores de atributos `state` e `selected` , que podem ser usados para aplicar capas diferentes a estados de botão diferentes. Particularmente, corresponde `selected='true'` ao estado &quot;silenciado&quot; e `selected='false'` corresponde ao estado &quot;silenciado&quot;.

A área da barra de volume vertical é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**Propriedades de CSS da área da barra de volume vertical**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo do volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> A altura do volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

A faixa dentro do controle de volume vertical é controlada com os seguintes seletores de classe CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Propriedades de CSS do controle de volume vertical**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo do controle de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do controle de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do controle de volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão de volume vertical é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Propriedades de CSS do botão de controle de volume vertical**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Arte-final do botão de controle de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão de controle de volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão de controlo do volume vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posição horizontal do botão de controlo de volume vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) da interface do usuário para obter mais informações.

## Exemplos {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um botão silencioso com 32 x 32 pixels e posicionado 6 pixels a partir da parte superior e 38 pixels a partir da borda direita da barra de controle. Exiba uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionado ou não selecionado.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

A seguir está um exemplo de como você pode estilizar o controle deslizante de volume dentro do controle de volume mutável.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Veja a seguir um exemplo de como você pode personalizar o player de vídeo para que o som seja desativado durante a reprodução. Adicione o seguinte código ao código incorporado do visualizador:

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

No exemplo de código acima, o nível de volume é definido como `0` no `mutableVolume` componente. Em seguida, o mesmo componente é desativado para que não possa ser usado pelo usuário final.
