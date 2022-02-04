---
title: Botão Ampliar
description: Clicar ou tocar nesse botão amplia o zoom de uma imagem na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: fc5a204f-74fd-43af-bb48-fe47eb99ab73
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Botão Ampliar{#zoom-in-button}

Clicar ou tocar nesse botão amplia o zoom de uma imagem na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

```
.s7spinviewer .s7zoominbutton
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
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
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
   <td colname="col2"> <p>Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta `state` seletor de atributos, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) para obter mais informações.

Exemplo - Para configurar um botão de zoom com 32 x 32 pixels e posicionar seis pixels da borda superior e direita do visualizador. E finalmente, exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7spinviewer .s7zoominbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7spinviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7spinviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7spinviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7spinviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```
