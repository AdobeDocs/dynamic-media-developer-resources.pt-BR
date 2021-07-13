---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> todas as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p> Quando definido como <span class="codeph"> 0</span>, somente as miniaturas visíveis são carregadas. </p> <p>Defina <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir quantas linhas invisíveis ao redor da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-4b7952997f9240e581d21bcdb173f9af}

Opcional.

## Padrão {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exemplo {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
