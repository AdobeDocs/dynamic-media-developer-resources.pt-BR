---
description: O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.
seo-description: O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.
seo-title: Destaque da focagem
solution: Experience Manager
title: Destaque da focagem
uuid: 56600f9c-c51e-40a4-93b6-a43902ef5ff1
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imagens interativas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# Destaque do foco{#focus-highlight}

O realce do foco de entrada exibido em torno do elemento da interface do usuário do visualizador focado é controlado com o seletor de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS**

A aparência é controlada com o seguinte seletor de classe CSS:

```
.s7interactiveimage *:focus
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
.s7interactiveimage *:focus { 
 outline: none; 
}
```

