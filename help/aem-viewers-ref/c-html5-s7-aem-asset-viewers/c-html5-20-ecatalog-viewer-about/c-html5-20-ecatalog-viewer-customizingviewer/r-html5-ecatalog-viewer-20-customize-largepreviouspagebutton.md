---
title: Botão Página anterior grande
description: Clicar ou tocar nesse botão traz o usuário para a página anterior no catálogo. Esse botão aparece na barra de controle principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 51c2fe1a-c14e-4a87-887b-f97546a517a4
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Botão Página anterior grande{#large-previous-page-button}

Selecionar ou tocar nesse botão traz o usuário para a página anterior no catálogo. Esse botão aparece na barra de controle principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton`

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
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda esquerda da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta `state` seletor de atributos, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de página anterior grande, com 56 x 56 pixels, centrado verticalmente e ancorado na borda esquerda do visualizador, e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton { 
bottom:50%; 
margin-bottom:-28px; 
left:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/LeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/LeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/LeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/LeftButton_dark_disabled.png); 
}
```
