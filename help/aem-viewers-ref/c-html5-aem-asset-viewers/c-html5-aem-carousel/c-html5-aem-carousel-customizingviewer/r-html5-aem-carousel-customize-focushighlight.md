---
title: Foco em destaque
description: O destaque do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focalizado é controlado com o seletor de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f9343055-9fd9-4b19-bba3-1f742acb6193
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Foco em destaque{#focus-highlight}

O destaque do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focalizado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS**

A aparência é controlada com o seguinte seletor de classe CSS:

```
.s7carouselviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> estrutura de tópicos </span> </p> </td> 
   <td colname="col2"> <p>Estilo de destaque da focagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para desativar o destaque de foco do navegador padrão para todos os elementos da interface do usuário do visualizador, adicione o seguinte seletor de CSS à folha de estilos do visualizador:

```
.s7carouselviewer *:focus { 
 outline: none; 
}
```
