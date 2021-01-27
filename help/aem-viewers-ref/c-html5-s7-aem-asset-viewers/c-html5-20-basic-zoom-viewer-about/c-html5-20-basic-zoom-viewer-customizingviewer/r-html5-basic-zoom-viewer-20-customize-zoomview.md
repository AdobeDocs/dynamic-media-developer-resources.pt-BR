---
description: A visualização principal consiste na imagem com zoom.
seo-description: A visualização principal consiste na imagem com zoom.
seo-title: Visualização de zoom
solution: Experience Manager
title: Visualização de zoom
topic: Dynamic Media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Visualização de zoom{#zoom-view}

A visualização principal consiste na imagem com zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>O cursor é exibido sobre a visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Em sistemas desktop, o componente suporta o seletor de atributos `cursortype` que pode ser aplicado à classe `.s7zoomview` e controla o tipo de cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` são suportados:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
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
   <td colname="col2"> <p>Exibida quando a imagem está no nível máximo de zoom e pode ser redefinida para seu estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrasto  </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando um usuário desloca a imagem que está no estado ampliado. </p> </td> 
  </tr> 
 </tbody> 
</table>

