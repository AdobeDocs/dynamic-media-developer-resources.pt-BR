---
description: Clicar ou tocar nesse botão gira a imagem para a direita na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Além disso, o botão fica oculto quando um conjunto de rotação multidimensional é usado. É possível dimensionar, usar a capa e posicionar o botão usando o CSS.
solution: Experience Manager
title: Botão girar para a direita
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,User
exl-id: 2e70ad27-9fce-4a18-b856-08aa6dbec3f2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Botão girar para a direita{#spin-right-button}

Clicar ou tocar nesse botão gira a imagem para a direita na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Além disso, o botão fica oculto quando um conjunto de rotação multidimensional é usado. É possível dimensionar, usar a capa e posicionar o botão usando o CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS dos botões giratórios**

O botão é adicionado a um contêiner interno controlado por DIV com o seletor de classe CSS:

```
.s7mixedmediaviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

A aparência desse botão dentro do contêiner é controlada com o seletor de classe CSS:

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

Exemplo - para configurar um botão girar à direita com 28 x 28 pixels, que é posicionado na borda direita do contêiner interno e que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton { 
 position:absolute; 
 right: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='up'] { 
background-image:url(images/v2/SpinRightButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='over'] { 
background-image:url(images/v2/SpinRightButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='down'] { 
 background-image:url(images/v2/SpinRightButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panrightbutton[state='disabled'] { 
 background-image:url(images/v2/SpinRightButton_light_disabled.png); 
}
```
