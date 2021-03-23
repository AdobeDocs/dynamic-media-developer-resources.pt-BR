---
description: Clicar ou tocar nesse botão gira a imagem para a direita na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Além disso, o botão fica oculto quando um conjunto de rotação multidimensional é usado. É possível dimensionar, usar a capa e posicionar o botão usando o CSS.
seo-description: Clicar ou tocar nesse botão gira a imagem para a direita na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Além disso, o botão fica oculto quando um conjunto de rotação multidimensional é usado. É possível dimensionar, usar a capa e posicionar o botão usando o CSS.
seo-title: Botão girar para a direita
solution: Experience Manager
title: Botão girar para a direita
uuid: 5c754e53-9311-4d4f-96e7-2bb9a5a7babf
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Botão girar para a direita{#spin-right-button}

Clicar ou tocar nesse botão gira a imagem para a direita na exibição principal. Este botão não é exibido em telefones celulares para salvar propriedades de tela. Além disso, o botão fica oculto quando um conjunto de rotação multidimensional é usado. É possível dimensionar, usar a capa e posicionar o botão usando o CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS dos botões giratórios**

O botão é adicionado a um contêiner interno controlado por DIV com o seletor de classe CSS:

```
.s7spinviewer .s7spinbuttons
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
.s7spinviewer .s7spinbuttons .s7panrightbutton
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
   <td colname="col2"> <p>Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) para obter mais informações.

Exemplo - para configurar um botão girar à direita com 28 x 28 pixels, que é posicionado na borda direita do contêiner interno e que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7spinviewer .s7spinbuttons .s7panrightbutton { 
 position:absolute; 
 right: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='up'] { 
background-image:url(images/v2/SpinRightButton_light_up.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='over'] { 
background-image:url(images/v2/SpinRightButton_light_over.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='down'] { 
 background-image:url(images/v2/SpinRightButton_light_down.png); 
} 
.s7spinviewer .s7spinbuttons .s7panrightbutton[state='disabled'] { 
 background-image:url(images/v2/SpinRightButton_light_disabled.png); 
}
```

