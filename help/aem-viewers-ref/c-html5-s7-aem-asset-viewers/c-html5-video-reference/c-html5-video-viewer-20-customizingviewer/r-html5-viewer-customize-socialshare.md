---
description: A ferramenta de compartilhamento em redes sociais é exibida no canto superior direito por padrão. Ele consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.
seo-description: A ferramenta de compartilhamento em redes sociais é exibida no canto superior direito por padrão. Ele consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.
seo-title: Compartilhamento em redes sociais
solution: Experience Manager
title: Compartilhamento em redes sociais
topic: Dynamic Media
uuid: 5c1ce7b4-54bf-486f-8b57-1d6d0cec119e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---


# Compartilhamento em redes sociais{#social-share}

A ferramenta de compartilhamento em redes sociais é exibida no canto superior direito por padrão. Ele consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho da ferramenta de compartilhamento em redes sociais na interface do usuário do visualizador são controlados com o seguinte:

```
.s7videoviewer .s7socialshare
```

**Propriedades de CSS da ferramenta de compartilhamento em redes sociais**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posição vertical da ferramenta de compartilhamento em redes sociais em relação ao container do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Posição horizontal da ferramenta de compartilhamento em redes sociais em relação ao container do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura da ferramenta de compartilhamento em redes sociais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da ferramenta de compartilhamento em redes sociais. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma ferramenta de compartilhamento em redes sociais que esteja posicionada a quatro pixels da parte superior e a cinco pixels da direita do container do visualizador e seja dimensionada para 28 x 28 pixels.

```
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

A aparência do botão da ferramenta de compartilhamento em redes sociais é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7socialshare .s7socialbutton
```

**Propriedades de CSS do botão social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - configure um botão de ferramenta de compartilhamento em redes sociais que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

A aparência do painel que contém os ícones individuais de compartilhamento em redes sociais é controlada pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7socialshare .s7socialsharepanel
```

**Propriedades de CSS do painel de compartilhamento em redes sociais**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um painel para ter uma cor transparente:

```
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

