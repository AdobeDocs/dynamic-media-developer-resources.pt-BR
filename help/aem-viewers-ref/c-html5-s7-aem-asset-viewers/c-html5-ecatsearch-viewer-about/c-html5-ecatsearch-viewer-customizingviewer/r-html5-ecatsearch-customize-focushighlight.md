---
title: Destaque da focagem
description: Destaque do foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Destaque da focagem{#focus-highlight}

Destaque do foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

A aparência do realce de foco é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer *:focus
```

**Propriedades CSS do realce de foco**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline </span> </p> </td> 
   <td colname="col2"> <p> Estilo do destaque de foco. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para desativar o realce de foco padrão do navegador para todos os elementos da interface do usuário do visualizador, adicione o seguinte seletor de CSS à folha de estilos do visualizador:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
