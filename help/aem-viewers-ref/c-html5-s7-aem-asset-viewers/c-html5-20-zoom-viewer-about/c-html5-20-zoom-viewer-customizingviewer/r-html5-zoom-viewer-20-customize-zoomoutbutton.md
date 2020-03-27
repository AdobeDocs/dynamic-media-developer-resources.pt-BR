---
description: Clicar ou tocar nesse botão diminui o zoom em uma imagem na visualização principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, exibir e posicionar esse botão usando o CSS.
seo-description: Clicar ou tocar nesse botão diminui o zoom em uma imagem na visualização principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, exibir e posicionar esse botão usando o CSS.
seo-title: Botão Menos zoom
solution: Experience Manager
title: Botão Menos zoom
topic: Dynamic media
uuid: 353577c1-df6b-45d9-9dfe-4363f18ed199
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Botão Menos zoom{#zoom-out-button}

Clicar ou tocar nesse botão diminui o zoom em uma imagem na visualização principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, exibir e posicionar esse botão usando o CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

```
.s7zoomviewer .s7zoomoutbutton
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
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo preenchimento. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de `state` atributos, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)da interface do usuário.

Exemplo - para configurar um botão de menos zoom com 32 x 32 pixels, posicionado seis pixels da borda superior e direita do visualizador, e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7zoomviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7zoomviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7zoomviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7zoomviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```

