---
title: Foco em destaque
description: O destaque do foco de entrada exibido em torno do elemento da interface do visualizador focalizado é controlado com o seletor de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 5849dc2f-d4df-40a2-82c9-454284308a04
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Foco em destaque{#focus-highlight}

O destaque do foco de entrada exibido em torno do elemento da interface do visualizador focalizado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS**

A aparência é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer *:focus
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
.s7flyoutviewer *:focus { 
 outline: none; 
}
```
