---
title: Botão Última página
description: Clicar ou tocar nesse botão leva o usuário para a última página no catálogo. Esse botão aparece na barra de controle principal em sistemas desktop e tablets; em telefones celulares, ele é adicionado a uma barra de controle secundária. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d133a5e2-4a39-41b6-a3fc-9d1b66c78752
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Botão Última página{#last-page-button}

Selecionar ou tocar nesse botão traz o usuário para a última página no catálogo. Esse botão aparece na barra de controle principal em sistemas desktop e tablets; em telefones celulares, ele é adicionado a uma barra de controle secundária. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7lastpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal (em sistemas desktop e tablets) ou da barra de controle secundária (em celulares), incluindo preenchimento. </p> </td> 
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão de última página com 28 x 28 pixels e posicionado a 4 pixels da parte inferior e a 220 pixels da borda esquerda da barra de controle principal. Por fim, o exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```
