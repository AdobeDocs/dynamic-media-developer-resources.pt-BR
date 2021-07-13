---
description: A ferramenta de compartilhamento facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais . Quando o botão é clicado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento Social .
solution: Experience Manager
title: Compartilhamento facebook
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Developer,User
exl-id: 343cde8b-796a-420f-abb7-268b3791a684
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Compartilhamento facebook{#facebook-share}

A ferramenta de compartilhamento facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais . Quando o botão é clicado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento Social .

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

A aparência do botão Compartilhar do Facebook é controlada com o seguinte seletor de classe CSS:

```
.s7video360viewer .s7facebookshare
```

**Propriedades de CSS da ferramenta de compartilhamento Facebook**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento do Social definindo `display:none` propriedade CSS em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemplo**  - Para configurar um botão de compartilhamento do Facebook com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
