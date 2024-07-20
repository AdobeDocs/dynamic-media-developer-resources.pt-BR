---
title: Compartilhamento de twitter
description: A ferramenta de compartilhamento de twitters consiste em um botão adicionado ao painel de compartilhamento social. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c7e84d40-a779-4747-b79a-3a40a622a445
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Compartilhamento de twitter{#twitter-share}

A ferramenta de compartilhamento de twitters consiste em um botão adicionado ao painel de compartilhamento social. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

A aparência do botão de compartilhamento de Twitter é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7twittershare
```

**Propriedades CSS da ferramenta de compartilhamento de Twitters**

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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento em redes sociais definindo a propriedade CSS `display:none` em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de compartilhamento de Twitter com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7ecatalogsearchviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
