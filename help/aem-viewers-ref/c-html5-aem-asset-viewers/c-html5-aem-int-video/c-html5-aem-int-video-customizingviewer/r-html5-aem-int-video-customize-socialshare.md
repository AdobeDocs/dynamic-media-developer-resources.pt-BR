---
title: Compartilhamento em redes sociais
description: A ferramenta de compartilhamento social aparece no canto superior direito por padrão. Consiste em um botão e um painel que é expandido quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Compartilhamento em redes sociais{#social-share}

A ferramenta de compartilhamento social aparece no canto superior direito por padrão. Consiste em um botão e um painel que é expandido quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho da ferramenta de compartilhamento social na interface do usuário do visualizador são controlados com o seguinte:

```
.s7interactivevideoviewer .s7socialshare
```

**Propriedades CSS da ferramenta de compartilhamento social**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posição vertical da ferramenta de compartilhamento em redes sociais em relação ao contêiner do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Posição horizontal da ferramenta de compartilhamento social em relação ao contêiner do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example}

Para configurar uma ferramenta de compartilhamento social que é posicionada quatro pixels da parte superior e cinco pixels à direita do contêiner do visualizador e é dimensionada 28 x 28 pixels.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

A aparência do botão de ferramenta de compartilhamento social é controlada pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**Propriedades CSS do botão de ferramenta de compartilhamento social**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Exemplo {#example-1}

Para configurar um botão de ferramenta de compartilhamento social que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

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

A aparência do painel que contém os ícones individuais de compartilhamento social é controlada pelo seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**Propriedades de CSS do painel de compartilhamento social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#example-2}

Para configurar um painel para ter uma cor transparente:

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
