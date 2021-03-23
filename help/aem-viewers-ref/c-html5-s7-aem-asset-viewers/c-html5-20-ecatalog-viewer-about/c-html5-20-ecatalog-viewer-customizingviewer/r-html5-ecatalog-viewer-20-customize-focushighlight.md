---
description: Destaque do foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focado.
seo-description: Destaque do foco de entrada exibido ao redor do elemento da interface do usuário do visualizador focado.
seo-title: Destaque da focagem
solution: Experience Manager
title: Destaque da focagem
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# Destaque do foco{#focus-highlight}

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
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
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

