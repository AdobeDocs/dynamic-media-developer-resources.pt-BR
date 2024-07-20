---
title: Exibição de favoritos
description: A visualização Favoritos consiste em uma coluna de imagens em miniatura.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Exibição de favoritos{#favorites-view}

A visualização Favoritos consiste em uma coluna de imagens em miniatura.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

A aparência do contêiner de visualização de favoritos é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

A posição e a altura da visualização Favoritos são gerenciadas pela visualização; no CSS, é possível definir apenas a largura.

**Propriedades CSS da exibição Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo da visualização Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da exibição. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma visualização de Favoritos com 100 pixels de largura e um plano de fundo cinza semitransparente.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

O espaçamento entre as miniaturas de Favoritos é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**Propriedades CSS das miniaturas de Favoritos**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem vertical ao redor de cada miniatura. O espaçamento real entre miniaturas é igual à soma das margens superior e inferior definidas para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o espaçamento de dez pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

A aparência da miniatura individual é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Propriedades CSS das miniaturas de Favoritos**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura dá suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Especificamente, `state="selected"` corresponde à miniatura selecionada recentemente pelo usuário. Enquanto `state="default"` corresponde ao restante das miniaturas. E `state="over"` é usado ao passar o mouse.

Exemplo - Para configurar miniaturas com 75 x 75 pixels, tenha uma borda padrão cinza-claro e uma borda selecionada cinza-escuro.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

A aparência do rótulo da miniatura é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Propriedades CSS do rótulo Favoritos**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar rótulos com uma fonte Helvetica® de 14 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
