---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '70'
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

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
