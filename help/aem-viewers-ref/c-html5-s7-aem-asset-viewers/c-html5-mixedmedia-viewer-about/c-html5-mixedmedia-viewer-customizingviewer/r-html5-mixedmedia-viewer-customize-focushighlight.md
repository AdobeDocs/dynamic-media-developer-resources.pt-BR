---
title: Foco em destaque
description: O destaque do foco de entrada exibido em torno do elemento da interface do visualizador focalizado é controlado com o seletor de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 7d29dab2-6f01-4328-9e92-0c370acaa2d6
TQID: 'https://experienceleague.adobe.com/JC7zBAfwq8rI4z8n8PNFjV5S2Xv-Tb91qs19oeEdsPI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# Foco em destaque{#focus-highlight}

O destaque do foco de entrada exibido em torno do elemento da interface do visualizador focalizado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS**

A aparência é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer *:focus
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
.s7mixedmediaviewer *:focus { 
 outline: none; 
}
```
