---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Defina como <span class="codeph"> 1</span> para ativar o pré-carregamento da imagem com zoom. </p> <p>Defina como <span class="codeph"> 0</span> para carregar a imagem do zoom de forma incremental, conforme necessário. </p> <p> <p>Se você habilitar essa opção, ela poderá resultar em um uso de largura de banda substancialmente maior, pois a imagem com zoom deve ser carregada em sua totalidade, mesmo que nenhuma ação de zoom seja executada pelo usuário. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
