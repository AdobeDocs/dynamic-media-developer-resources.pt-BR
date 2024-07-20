---
title: Área do visualizador principal
description: A área de exibição principal é a área ocupada pela exibição da imagem suspensa e pelas amostras.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: ab1653a3-38e6-49bb-97b7-005304349ec9
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# Área do visualizador principal{#main-viewer-area}

A área de exibição principal é a área ocupada pela exibição da imagem suspensa e pelas amostras.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer
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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um visualizador de imagem suspensa com plano de fundo branco ( `#FFFFFF`) e definir seu tamanho como 260 x 500 pixels.

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```
