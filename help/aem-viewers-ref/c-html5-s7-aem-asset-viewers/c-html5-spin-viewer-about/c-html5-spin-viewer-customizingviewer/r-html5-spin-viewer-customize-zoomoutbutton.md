---
title: Botão de menos zoom
description: Clicar ou tocar neste botão diminui o zoom em uma imagem na exibição principal. Esse botão não é exibido em telefones celulares para salvar o espaço na tela. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2de7ab27-029b-496d-8696-21e554effa66
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Botão de menos zoom{#zoom-out-button}

Clicar ou tocar neste botão diminui o zoom em uma imagem na exibição principal. Esse botão não é exibido em telefones celulares para salvar o espaço na tela. Você pode dimensionar, aplicar capa e posicionar esse botão usando CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

```
.s7spinviewer .s7zoomoutbutton
```

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
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
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
   <td colname="col2"> <p>Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) para obter mais informações.

Exemplo - Para configurar um botão de diminuição de zoom com 32 x 32 pixels e posicionado a seis pixels da borda superior e direita do visualizador. Por fim, o exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7spinviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7spinviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7spinviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7spinviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7spinviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```
