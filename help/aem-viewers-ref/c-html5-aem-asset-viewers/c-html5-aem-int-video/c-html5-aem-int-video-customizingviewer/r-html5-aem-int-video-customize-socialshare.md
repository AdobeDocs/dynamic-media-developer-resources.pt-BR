---
title: Compartilhamento social
description: Por padrão, a ferramenta de compartilhamento em redes sociais é exibida no canto superior direito. Consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Compartilhamento social{#social-share}

Por padrão, a ferramenta de compartilhamento em redes sociais é exibida no canto superior direito. Consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho da ferramenta de compartilhamento social na interface do usuário do visualizador são controlados com o seguinte:

```
.s7interactivevideoviewer .s7socialshare
```

**Propriedades CSS da ferramenta de compartilhamento social**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posição vertical da ferramenta de compartilhamento em redes sociais em relação ao contêiner do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p> Posição horizontal da ferramenta de compartilhamento em redes sociais em relação ao container do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example}

Para configurar uma ferramenta de compartilhamento em redes sociais posicionada a quatro pixels da parte superior e a cinco pixels da direita do contêiner do visualizador e dimensionada a 28 x 28 pixels.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

A aparência do botão de ferramenta de compartilhamento em redes sociais é controlada com o seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**Propriedades CSS do botão de ferramenta de compartilhamento social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Exemplo {#example-1}

Para configurar um botão de ferramenta de compartilhamento em redes sociais que exiba uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

A aparência do painel que contém os ícones individuais de compartilhamento em redes sociais é controlada com o seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**Propriedades CSS do painel de compartilhamento social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-2}

Para configurar um painel para ter cor transparente:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
