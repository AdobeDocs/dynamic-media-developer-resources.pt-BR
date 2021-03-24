---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 2%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Defina como <span class="codeph"> 1</span> para ativar o pré-carregamento da imagem com zoom ou defina como <span class="codeph"> 0</span> para carregar a imagem de zoom de forma incremental, conforme necessário. </p> <p> <p>Observação:  Se você habilitar essa opção, poderá resultar em um uso substancialmente maior da largura de banda. A imagem com zoom é carregada em sua totalidade, mesmo se o usuário não iniciar uma ação de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
