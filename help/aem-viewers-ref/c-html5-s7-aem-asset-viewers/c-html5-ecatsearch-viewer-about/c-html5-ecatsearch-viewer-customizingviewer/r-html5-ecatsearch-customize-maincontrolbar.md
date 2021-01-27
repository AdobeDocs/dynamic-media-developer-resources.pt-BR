---
description: A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Pesquisa de eCatalog.
seo-description: A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Pesquisa de eCatalog.
seo-title: Barra de controle principal
solution: Experience Manager
title: Barra de controle principal
topic: Dynamic Media
uuid: 21b6e6cd-115f-4c7b-a61e-34b307142045
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---


# Barra de controle principal{#main-control-bar}

A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Pesquisa de eCatalog.

Em telefones celulares, ainda mantém os botões Miniaturas, Índice, Download, Imprimir, Favoritos, Compartilhamento em redes sociais, Tela cheia e Fechar. No entanto, os botões Primeira página e Última página e Indicador de página são removidos da barra de controle principal e adicionados à barra de controle secundária. Por padrão, a barra de controle principal é exibida na parte superior da área do visualizador em sistemas de desktop e telefones celulares e movida para a parte inferior da área do visualizador em tablets. Sempre leva a largura total do visualizador disponível. É possível alterar sua cor, altura e posição vertical no CSS, em relação ao container do visualizador.

A aparência da barra de controle principal é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo da barra de controle principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - para configurar uma barra de controle principal cinza com 36 pixels de altura e posicionada na parte superior do container do visualizador.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

A barra de controle principal suporta um recurso de rolagem opcional. Ela é ativada se a largura do visualizador for muito pequena e não houver espaço suficiente para ajustar todos os botões predefinidos na barra de controle. Nesse caso, um botão de seta de dois estados é exibido no lado direito da barra de controle. Clicar ou tocar nesse botão rola todos os elementos da barra de controle para a esquerda ou para a direita, dependendo do estado do botão de rolagem. O caso de uso principal desse recurso são dispositivos móveis com telas pequenas na orientação retrato.

O recurso de rolagem está ativado para a barra de controle principal e é desativado para a barra de controle secundária. O recurso é ativado e desativado usando o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>Quando definido como <span class="codeph"> static </span>, o recurso de rolagem será desativado. </p> <p>Defina essa propriedade como <span class="codeph"> absoluto </span> para ativar o recurso de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão de rolagem é adicionado a um elemento de container especial que posiciona o botão corretamente e permite estilizar a área ao redor do botão de forma diferente do restante do plano de fundo da barra de controle, caso a altura do botão de rolagem seja menor que a altura da barra de controle.

A aparência desse container de botão de rolagem é controlada pelo seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalmente deve ser igual ou maior que a largura do próprio botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode dimensionar e inserir a capa do botão de rolagem por meio do CSS.

A aparência desse botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta os seletores de atributos `state` e `selected`, que podem ser usados para aplicar diferentes capas a diferentes estados de botão. Em particular, `state="selected"` corresponde ao estado inicial do botão de rolagem quando é possível rolar o conteúdo da barra de controle para a esquerda; `state="default"` corresponde ao estado em que o conteúdo é rolado completamente para a esquerda e o botão de rolagem sugere que ele retorne ao estado inicial.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

**Exemplo**  - para ativar o recurso de rolagem na barra de controle principal para telefones celulares e configurar um botão de rolagem com 64 x 64 pixels que exibe uma imagem diferente para cada um dos 4 estados de botão diferentes quando selecionado ou não selecionado:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

