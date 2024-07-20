---
title: Compartilhamento facebook
description: A ferramenta de compartilhamento do facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 343cde8b-796a-420f-abb7-268b3791a684
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Compartilhamento facebook{#facebook-share}

A ferramenta de compartilhamento do facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

A aparência do botão de compartilhamento do Facebook é controlada com o seguinte seletor de classe CSS:

```
.s7video360viewer .s7facebookshare
```

**Propriedades CSS da ferramenta de compartilhamento do Facebook**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento em redes sociais definindo a propriedade CSS `display:none` em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Exemplo** - Para configurar um botão de compartilhamento do Facebook com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes:

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
