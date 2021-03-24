---
description: Botão Pesquisar
solution: Experience Manager
title: Botão Pesquisar
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Botão Pesquisar{#search-button}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência do botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7searchbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da parte superior da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p> A distância até ao botão seguinte à esquerda ou à esquerda da barra de controle, se este for o primeiro botão de uma linha. </p> </td> 
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
>Esse botão suporta os seletores de atributos `state` e `selected`, que podem ser usados para aplicar capas diferentes a estados de botão diferentes.
>
>Especificamente, `selected='false'` corresponde ao estado inicial do botão de rolagem e `selected='true'` corresponde ao estado quando o painel de pesquisa está ativo.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de Pesquisa com 28 x 28 pixels e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionado ou não selecionado.

```
.s7ecatalogsearchviewer .s7searchbutton{ 
 margin-top: 4px; 
 margin-left: 10px; 
 width:28px; 
 height:28px;  
 display: inline-block; 
 background-size:contain; 
} 
 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/Search_dark_up.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/Search_dark_down.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/Search_dark_over.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png);  
}
```

