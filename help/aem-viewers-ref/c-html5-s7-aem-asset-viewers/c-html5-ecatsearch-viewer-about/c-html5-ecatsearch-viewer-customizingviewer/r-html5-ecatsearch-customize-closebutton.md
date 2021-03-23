---
description: Clicar ou tocar nesse botão fecha a página da Web contêiner. Esse botão só aparecerá se o parâmetro closebutton estiver definido como 1. Este botão não está disponível em sistemas de desktop. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.
seo-description: Clicar ou tocar nesse botão fecha a página da Web contêiner. Esse botão só aparecerá se o parâmetro closebutton estiver definido como 1. Este botão não está disponível em sistemas de desktop. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.
seo-title: Botão Fechar
solution: Experience Manager
title: Botão Fechar
uuid: 312325a8-e10d-4c9f-a008-18ab666fbdd2
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Botão Fechar{#close-button}

Clicar ou tocar nesse botão fecha a página da Web contêiner. Esse botão só aparecerá se o parâmetro closebutton estiver definido como 1. Este botão não está disponível em sistemas de desktop. Você pode dimensionar, aplicar a capa e posicionar esse botão usando o CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7closebutton`

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
   <td colname="col2"> <p>Posição a partir da borda superior da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda esquerda da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior da barra de controle principal, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
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
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de fechamento com 56 x 56 pixels, posicionado 4 pixels da parte superior e direita da barra de controle principal e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogsearchviewer .s7closebutton { 
top:4px; 
right:4px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```

