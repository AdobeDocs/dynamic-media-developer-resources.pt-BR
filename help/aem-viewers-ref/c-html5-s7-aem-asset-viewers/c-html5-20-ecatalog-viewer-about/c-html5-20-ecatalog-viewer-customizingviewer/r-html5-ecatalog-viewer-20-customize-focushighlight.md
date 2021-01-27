---
description: Destaque de foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focalizado.
seo-description: Destaque de foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focalizado.
seo-title: Destaque do foco
solution: Experience Manager
title: Destaque do foco
topic: Dynamic Media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Destaque do foco{#focus-highlight}

Destaque de foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focalizado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

A aparência do realce de foco é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer *:focus
```

**Propriedades de CSS do destaque de foco**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> esboço  </span> </p> </td> 
   <td colname="col2"> <p> Estilo de realce do foco. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para desativar o realce de foco padrão do navegador para todos os elementos da interface do usuário do visualizador, adicione o seguinte seletor de CSS à folha de estilos do visualizador:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

