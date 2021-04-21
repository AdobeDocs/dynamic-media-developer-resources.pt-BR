---
description: O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.
solution: Experience Manager
title: Destaque da focagem
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Destaque do foco{#focus-highlight}

O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS**

A aparência é controlada com o seguinte seletor de classe CSS:

```
.s7interactivevideoviewer *:focus
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
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```
