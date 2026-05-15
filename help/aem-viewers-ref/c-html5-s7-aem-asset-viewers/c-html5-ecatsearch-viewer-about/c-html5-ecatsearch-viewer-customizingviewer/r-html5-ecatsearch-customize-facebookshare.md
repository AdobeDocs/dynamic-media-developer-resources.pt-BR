---
title: Compartilhamento no Facebook
description: A ferramenta de compartilhamento do Facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 792d53de-5561-48bb-85d7-fbf3b6377673
TQID: 'https://experienceleague.adobe.com/6b-Gzzhw-sVfmRGdiU5qGC3-ICbDkIXIhce-pv043o0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 234
ht-degree: 0%

---

# Compartilhamento no Facebook{#facebook-share}

A ferramenta de compartilhamento do Facebook consiste em um botão adicionado ao painel Compartilhamento em redes sociais. Quando o botão é selecionado, o usuário é redirecionado para uma caixa de diálogo de compartilhamento fornecida por um serviço social. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

A aparência do botão de compartilhamento do Facebook é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7facebookshare
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento em redes sociais definindo a propriedade CSS `display:none` em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de compartilhamento do Facebook com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7ecatalogsearchviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
