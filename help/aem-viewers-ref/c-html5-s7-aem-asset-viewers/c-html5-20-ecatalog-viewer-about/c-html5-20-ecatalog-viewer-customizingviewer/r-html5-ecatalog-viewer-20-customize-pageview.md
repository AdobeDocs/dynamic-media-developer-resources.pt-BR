---
description: A visualização principal consiste na imagem do catálogo. Ele pode ser arrastado com o dedo para chegar a outra página ou ampliado.
seo-description: A visualização principal consiste na imagem do catálogo. Ele pode ser arrastado com o dedo para chegar a outra página ou ampliado.
seo-title: Visualização da página
solution: Experience Manager
title: Visualização da página
topic: Dynamic Media
uuid: 5e247f56-f0da-487b-8e03-587b9d36aa39
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# Visualização de página{#page-view}

A visualização principal consiste na imagem do catálogo. Ele pode ser arrastado com o dedo para chegar a outra página ou ampliado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo da visualização principal em formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>O cursor que é exibido sobre a visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Em sistemas desktop, o componente suporta o seletor de atributos `cursortype` que pode ser aplicado à classe `.s7pageview` e controla o tipo de cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` são suportados:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem não tem zoom devido a uma pequena resolução de imagem, configurações de componente ou ambos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem pode ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem está no nível máximo de zoom e pode ser redefinida para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrasto  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário desloca a imagem que está no estado ampliado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário realiza uma troca de imagem ao deslizar ou piscar na horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

O divisor de página que separa visualmente as páginas esquerda e direita da página espelhada do catálogo é controlado pelo seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do divisor de página. Defina para <span class="codeph"> 0 </span> px para ocultar o divisor completamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>A imagem que você deseja usar como divisor de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para ter divisor de página de largura de 40 pixels com imagem semitransparente.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Quando o modificador `frametransition` estiver definido como `turn` ou `auto` (em sistemas de desktop), a aparência do divisor de página será controlada pelo modificador `pageturnstyle` e a classe CSS `.s7pagedivider` será ignorada.

É possível configurar a exibição dos cursores personalizados do mouse sobre a área do visualizador principal. Isso é controlado com seletores de atributos adicionais aplicados à classe `.s7ecatalogviewer .s7pageview` CSS:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p> Normalmente, uma seta é exibida para uma imagem sem zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando uma imagem pode ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando uma imagem está com o zoom máximo e pode ser redefinida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrasto  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário executa a operação de arrastar com zoom na imagem </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário realiza a troca de imagem usando o gesto de slide </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - tem cursores de mouse diferentes para cada tipo de estado do componente.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```

