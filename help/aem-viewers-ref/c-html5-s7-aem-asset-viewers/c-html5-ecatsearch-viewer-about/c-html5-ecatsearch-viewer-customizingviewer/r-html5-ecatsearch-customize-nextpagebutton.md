---
title: Botão Próxima página
description: Selecionar esse botão traz o usuário para a próxima página no catálogo. Esse botão aparece na barra de controle principal. Este botão não é exibido em telefones celulares para salvar o espaço na tela. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 6b94e583-fb2a-4010-bfc6-4fa901252e4e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Botão Próxima página{#next-page-button}

Selecionar esse botão traz o usuário para a próxima página no catálogo. Esse botão aparece na barra de controle principal. Este botão não é exibido em telefones celulares para salvar o espaço na tela. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal, incluindo o preenchimento. </p> </td> 
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
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
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

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão de próxima página com 28 x 28 pixels e posicionado a 4 pixels da parte inferior e a 250 pixels da borda direita da barra de controle principal. Por fim, o exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton { 
bottom:4px; 
right:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/ToolBarRightButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/ToolBarRightButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/ToolBarRightButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarRightButton_dark_disabled.png); 
}
```
