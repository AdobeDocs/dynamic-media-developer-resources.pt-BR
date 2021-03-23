---
description: A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Catálogo eletrônico.
seo-description: A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Catálogo eletrônico.
seo-title: Barra de controle principal
solution: Experience Manager
title: Barra de controle principal
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# Barra de controle principal{#main-control-bar}

A barra de controle principal é a área retangular em sistemas de desktop e tablets que contêm todos os controles da interface do usuário (exceto botões Página grande) disponíveis para o visualizador de Catálogo eletrônico.

Em telefones celulares, ainda mantém miniaturas, Índice, Download, Imprimir, Favoritos, Compartilhamento em redes sociais, Tela cheia e Fechar botões. No entanto, os botões Primeira e Última página e Indicador de página são removidos da barra de controle principal e adicionados à barra de controle secundária. Por padrão, a barra de controle principal é exibida na parte superior da área do visualizador em sistemas de desktop e telefones celulares e movida para a parte inferior da área do visualizador em tablets. Ele sempre utiliza a largura total do visualizador disponível. É possível alterar a cor, a altura e a posição vertical no CSS, em relação ao contêiner do visualizador.

A aparência da barra de controle principal é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7controlbar`

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
   <td colname="col2"> <p>Posicione a partir da parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo da barra de controle principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**  - para configurar uma barra de controle principal cinza com 36 pixels de altura e que esteja posicionada na parte superior do contêiner do visualizador.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

A barra de controle principal suporta um recurso de rolagem opcional. Ela será ativada se a largura do visualizador for muito pequena e não houver espaço suficiente para ajustar todos os botões predefinidos na barra de controle. Nesse caso, um botão de seta de dois estados é exibido no lado direito da barra de controle. Clicar ou tocar nesse botão rola todos os elementos da barra de controle para a esquerda ou para a direita, dependendo do estado do botão de rolagem. Os principais casos de uso desse recurso são dispositivos móveis com telas pequenas na orientação retrato.

O recurso de rolagem é ativado para a barra de controle principal e está desativado para a barra de controle secundária. O recurso é ativado e desativado usando o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

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
   <td colname="col2"> <p>Quando definido como <span class="codeph"> estático </span>, o recurso de rolagem é desativado. </p> <p>Defina essa propriedade como <span class="codeph"> absoluto </span> para ativar o recurso de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão de rolagem é adicionado a um elemento de contêiner especial que posiciona o botão corretamente e permite estilizar a área ao redor do botão de forma diferente do restante do plano de fundo da barra de controle, caso a altura do botão de rolagem seja menor que a altura da barra de controle.

A aparência desse contêiner do botão de rolagem é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do contêiner. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode dimensionar e esfolar o botão de rolagem por meio de CSS.

A aparência desse botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta os seletores de atributos `state` e `selected`, que podem ser usados para aplicar capas diferentes a estados de botão diferentes. Em particular, `state="selected"` corresponde ao estado inicial do botão de rolagem quando é possível rolar o conteúdo da barra de controle para a esquerda; `state="default"` corresponde ao estado em que o conteúdo é rolado até a esquerda e o botão de rolagem sugere retorná-lo ao estado inicial.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

**Exemplo**  - para ativar o recurso de rolagem na barra de controle principal de telefones celulares e configurar um botão de rolagem com 64 x 64 pixels que exibe uma imagem diferente para cada um dos 4 estados de botão diferentes quando selecionado ou não selecionado:

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

