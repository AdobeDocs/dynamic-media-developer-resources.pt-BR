---
description: O realce de foco de entrada exibido em torno do elemento de interface do visualizador focalizado é controlado com o seletor de classe CSS.
seo-description: O realce de foco de entrada exibido em torno do elemento de interface do visualizador focalizado é controlado com o seletor de classe CSS.
seo-title: Destaque do foco
solution: Experience Manager
title: Destaque do foco
topic: Dynamic media
uuid: 81bf9937-6a26-4f69-838e-5ba41608ac09
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# Destaque do foco{#focus-highlight}

O realce de foco de entrada exibido em torno do elemento de interface do visualizador focalizado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS**

A aparência é controlada pelo seguinte seletor de classe CSS:

```
.s7spinviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> esboço  </span> </p> </td> 
   <td colname="col2"> <p>Estilo de realce do foco. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para desativar o realce de foco padrão do navegador para todos os elementos da interface do usuário do visualizador, adicione o seguinte seletor de CSS à folha de estilos do visualizador:

```
.s7spinviewer *:focus { 
 outline: none; 
}
```

