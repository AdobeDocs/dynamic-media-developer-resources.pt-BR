---
title: Área do visualizador principal
description: A área de exibição principal é a área ocupada pela exibição da imagem suspensa e pelas amostras.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bf928c22-23e9-4df3-b2d7-0841c64baf19
TQID: 'https://experienceleague.adobe.com/iTifzWseBM5X6r7i7dnP5TQ-NkwNnH-aDjPl-v7gjHM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
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
