---
description: O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.
solution: Experience Manager
title: Destaque da focagem
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,Business Practitioner
exl-id: 7d29dab2-6f01-4328-9e92-0c370acaa2d6
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# Destaque da focagem{#focus-highlight}

O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS**

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
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p>Estilo do destaque de foco. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para desativar o realce de foco padrão do navegador para todos os elementos da interface do usuário do visualizador, adicione o seguinte seletor de CSS à folha de estilos do visualizador:

```
.s7mixedmediaviewer *:focus { 
 outline: none; 
}
```
