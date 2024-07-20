---
title: Exibição de página
description: A exibição principal consiste na imagem do catálogo. Ele pode ser deslizado para chegar a outra página ou ampliado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Exibição de página{#page-view}

A exibição principal consiste na imagem do catálogo. Ele pode ser deslizado para chegar a outra página ou ampliado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo da visualização principal em formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor que é exibido sobre a exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Em sistemas desktop, o componente oferece suporte ao seletor de atributos `cursortype` que pode ser aplicado à classe `.s7pageview` e controla o tipo de cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` têm suporte:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padrão </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem não é ampliada devido a uma pequena resolução de imagem, configurações de componente ou ambas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando é possível ampliar a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redefiniu </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem está no nível de zoom máximo e pode ser redefinida para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastar </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário expande a imagem que está no estado ampliado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando o usuário executa uma troca de imagem passando o dedo horizontal ou o toque. </p> </td> 
  </tr> 
 </tbody> 
</table>

O divisor de página que separa visualmente as páginas esquerda e direita da página espelhada do catálogo é controlado com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura do divisor de página. Defina como <span class="codeph"> 0 </span> px para ocultar o divisor completamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem que você deseja usar como divisor de página. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - ter um divisor de página de 40 pixels de largura com imagem semitransparente.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Quando o modificador `frametransition` é definido como `turn` ou `auto` (em sistemas desktop), a aparência do divisor de página é controlada com o modificador `pageturnstyle` e a classe CSS `.s7pagedivider` é ignorada.

É possível configurar a exibição do cursor do mouse personalizado sobre a área do visualizador principal. Essa funcionalidade é controlada com os seletores de atributos adicionais aplicados à classe CSS `.s7ecatalogviewer .s7pageview`:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padrão </span> </p> </td> 
   <td colname="col2"> <p> Normalmente, uma seta é exibida para imagens sem zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Mostra quando uma imagem pode ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redefiniu </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando uma imagem está no zoom máximo e pode ser redefinida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastar </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário executa a operação de arrastar na imagem com zoom </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide </span> </p> </td> 
   <td colname="col2"> <p>Mostra quando o usuário executa a troca de imagem usando o gesto do slide </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - ter cursores de mouse diferentes para cada tipo de estado do componente.

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
