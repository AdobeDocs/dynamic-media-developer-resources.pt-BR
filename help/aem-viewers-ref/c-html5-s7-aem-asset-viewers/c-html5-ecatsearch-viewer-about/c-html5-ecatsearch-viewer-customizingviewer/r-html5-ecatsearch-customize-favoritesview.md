---
description: A visualização Favoritos consiste em uma coluna de imagens em miniatura.
seo-description: A visualização Favoritos consiste em uma coluna de imagens em miniatura.
seo-title: Visualização Favoritos
solution: Experience Manager
title: Visualização Favoritos
topic: Dynamic Media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Visualização favorita{#favorites-view}

A visualização Favoritos consiste em uma coluna de imagens em miniatura.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

A aparência da visualização favorita é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview
```

A posição e a altura da visualização Favoritos são geridas pela visualização; em CSS, é possível definir somente a largura.

**Propriedades de CSS da visualização Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo da visualização Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura da visualização. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma visualização Favoritos com 100 pixels de largura com um plano de fundo cinza semitransparente.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

O espaçamento entre miniaturas Favoritos é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**Propriedades de CSS das miniaturas Favoritos**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem vertical ao redor de cada miniatura. O espaçamento real das miniaturas é igual à soma das margens superior e inferior definidas para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o espaçamento de 10 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

A aparência da miniatura individual é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**Propriedades de CSS das miniaturas Favoritos**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira  </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de miniaturas. Especificamente, `state="selected"` corresponde à miniatura recentemente selecionada pelo usuário. `state="default"` corresponde ao resto das miniaturas. E `state="over"` é usado ao passar o mouse.

Exemplo - para configurar miniaturas com 75 x 75 pixels, uma borda padrão cinza claro e uma borda cinza escura selecionada.

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

A aparência da etiqueta em miniatura é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**Propriedades de CSS do rótulo Favoritos**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar rótulos com uma fonte Helvetica de 14 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

