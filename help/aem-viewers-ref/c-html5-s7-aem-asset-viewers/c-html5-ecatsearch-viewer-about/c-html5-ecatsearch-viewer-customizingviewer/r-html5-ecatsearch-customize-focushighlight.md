---
description: Destaque de foco de entrada exibido em torno do elemento da interface do usuário do visualizador focalizado.
seo-description: Destaque de foco de entrada exibido em torno do elemento da interface do usuário do visualizador focalizado.
seo-title: Destaque do foco
solution: Experience Manager
title: Destaque do foco
topic: Dynamic media
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Destaque do foco{#focus-highlight}

Destaque de foco de entrada exibido em torno do elemento da interface do usuário do visualizador focalizado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

A aparência do realce de foco é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer *:focus
```

**Propriedades de CSS do destaque de foco**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> esboço </span> </p> </td> 
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

