---
title: Exibição da página
description: A exibição principal consiste na imagem do catálogo. Ele pode ser deslizado para chegar a outra página ou ampliado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Exibição da página{#page-view}

A exibição principal consiste na imagem do catálogo. Ele pode ser deslizado para chegar a outra página ou ampliado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo da exibição principal em formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor que é exibido sobre a exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Em sistemas de desktop, o componente suporta o `cursortype` seletor de atributos que pode ser aplicado a `.s7pageview` e controla o tipo do cursor com base no estado do componente e na ação do usuário. O seguinte `cursortype` são compatíveis:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Exibida quando a imagem não é ampliável devido a uma pequena resolução de imagem, configurações de componente ou ambos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem puder ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redefinir </span> </p> </td> 
   <td colname="col2"> <p>Exibida quando a imagem está no nível máximo de zoom e pode ser redefinida para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastar </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário expande a imagem que está no estado com zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário realiza uma troca de imagem ao deslizar ou piscar na horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

O divisor de página que separa visualmente as páginas esquerda e direita do spread do catálogo é controlado com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

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
   <td colname="col2"> <p> A largura do divisor de página. Defina como <span class="codeph"> 0 </span> px para ocultar completamente o divisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem que você deseja usar como o divisor de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para ter divisor de página de 40 pixels de largura com imagem semitransparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Quando a variável `frametransition` modificador está definido como `turn` ou `auto` (em sistemas de desktop), a aparência do divisor de página é controlada com o `pageturnstyle` modificador e o `.s7pagedivider` A classe CSS é ignorada.

É possível configurar a exibição do cursor do mouse personalizado sobre a área principal do visualizador. Essa capacidade é controlada com os seletores de atributos adicionais aplicados à `.s7ecatalogsearchviewer .s7pageview` Classe CSS:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> Normalmente, uma seta é exibida para imagens sem zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando uma imagem pode ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redefinir </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando uma imagem está no zoom máximo e pode ser redefinida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastar </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário executa a operação de arrastar com zoom na imagem </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário realiza a troca de imagem usando gesto de slide </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - tem cursores de mouse diferentes para cada tipo de estado de componente.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
