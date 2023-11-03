---
title: Barra de controle principal
description: A barra de controle principal é a área retangular nos sistemas de desktop e tablets que contém todos os controles da interface do usuário (exceto botões de Página grande) disponíveis para o visualizador do eCatalog Search.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Barra de controle principal{#main-control-bar}

A barra de controle principal é a área retangular nos sistemas de desktop e tablets que contém todos os controles da interface do usuário (exceto botões de Página grande) disponíveis para o visualizador do eCatalog Search.

Nos telefones celulares, ele ainda mantém as miniaturas, o índice, os botões Download, Imprimir, Favoritos, Compartilhamento em redes sociais, tela cheia e Fechar. No entanto, os botões Primeira e Última página e o Indicador de página são removidos da barra de controle principal e adicionados à barra de controle secundária. Por padrão, a barra de controle principal é exibida na parte superior da área do visualizador em sistemas desktop e celulares, e movida para a parte inferior da área do visualizador em tablets. Leva sempre toda a largura disponível do visualizador. É possível alterar sua cor, altura e posição vertical no CSS, em relação ao contêiner do visualizador.

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
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo da barra de controle principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo** - para configurar uma barra de controle principal cinza com 36 pixels de altura e posicionada na parte superior do contêiner do visualizador.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

A barra de controle principal é compatível com um recurso de rolagem opcional. Ela será ativada se a largura do visualizador for muito pequena e não houver espaço suficiente para ajustar todos os botões predefinidos na barra de controle. Nesse caso, um botão de seta de dois estados é exibido no lado direito da barra de controle. Clicar ou tocar nesse botão rola todos os elementos da barra de controle para a esquerda ou para a direita, dependendo do estado do botão de rolagem. O principal caso de uso desse recurso são dispositivos móveis com telas pequenas na orientação retrato.

O recurso de rolagem está habilitado para a barra de controle principal e desabilitado para a barra de controle secundária. O recurso é ativado e desativado usando o seguinte seletor de classe CSS:

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
   <td colname="col2"> <p>Quando definido como <span class="codeph"> estático </span> o recurso de rolagem está desativado. </p> <p>Defina esta propriedade como <span class="codeph"> absoluto </span> para ativar o recurso de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão de rolagem é adicionado a um elemento de contêiner especial que posiciona o botão corretamente. Ela permite estilizar a área ao redor do botão de forma diferente do restante do plano de fundo da barra de controle, caso a altura do botão de rolagem seja menor que a altura da barra de controle.

A aparência desse contêiner de botão de rolagem é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Normalmente deve ser igual ou maior que a largura do próprio botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo do contêiner. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode dimensionar e aplicar capa ao próprio botão de rolagem por meio do CSS.

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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão oferece suporte ao `state` e `selected` seletores de atributo, que podem ser usados para aplicar capas diferentes a estados de botão diferentes. Em especial, `state="selected"` corresponde ao estado inicial do botão de rolagem quando é possível rolar o conteúdo da barra de controle para a esquerda. A variável `state="default"` corresponde ao estado quando o conteúdo é rolado totalmente para a esquerda, e o botão de rolagem sugere retorná-lo ao estado inicial.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

**Exemplo** - Para ativar o recurso de rolagem na barra de controle principal para telefones celulares. E configure um botão de rolagem com 64 x 64 pixels que exiba uma imagem diferente para cada um dos 4 estados de botão diferentes quando selecionado ou não selecionado:

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
