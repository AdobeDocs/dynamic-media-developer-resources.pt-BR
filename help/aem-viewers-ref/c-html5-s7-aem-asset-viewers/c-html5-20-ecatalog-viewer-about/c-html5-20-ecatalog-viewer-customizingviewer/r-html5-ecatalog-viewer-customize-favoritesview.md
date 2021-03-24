---
description: A exibição Favoritos consiste em uma coluna de imagens em miniatura.
solution: Experience Manager
title: Exibição de favoritos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Exibição de favoritos{#favorites-view}

A exibição Favoritos consiste em uma coluna de imagens em miniatura.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

A aparência do contêiner de exibição Favoritos é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesview
```

A posição e a altura da exibição Favoritos são gerenciadas pela exibição; em CSS, só é possível definir a largura.

**Propriedades CSS da exibição Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo da exibição Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura da exibição. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma exibição Favoritos com 100 pixels de largura com um plano de fundo cinza semitransparente.

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

O espaçamento entre miniaturas Favoritos é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**Propriedades CSS das miniaturas Favoritas**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem vertical em torno de cada miniatura. O espaçamento real da miniatura é igual à soma da margem superior e inferior definida para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um espaçamento de 10 pixels.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

A aparência da miniatura individual é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**Propriedades CSS das miniaturas Favoritas**

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
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura é compatível com o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Especificamente, `state="selected"` corresponde à miniatura recentemente selecionada pelo usuário. `state="default"` corresponde ao restante das miniaturas. E `state="over"` é usado no mouse.

Exemplo - para configurar miniaturas com 75 x 75 pixels, tenha uma borda padrão cinza-claro e uma borda cinza-escura selecionada.

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

A aparência do rótulo de miniatura é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**Propriedades CSS do rótulo Favoritos**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar rótulos com uma fonte Helvetica de 14 pixels.

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

