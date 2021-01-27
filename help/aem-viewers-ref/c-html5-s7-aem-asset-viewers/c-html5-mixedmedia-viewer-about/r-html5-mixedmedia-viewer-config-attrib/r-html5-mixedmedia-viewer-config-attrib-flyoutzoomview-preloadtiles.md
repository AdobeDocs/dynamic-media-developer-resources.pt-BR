---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic Media
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 3%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Defina como <span class="codeph"> 1</span> para ativar o pré-carregamento da imagem com zoom. </p> <p>Defina como <span class="codeph"> 0</span> para carregar a imagem de zoom incrementalmente, conforme necessário. </p> <p> <p>Observação:  Esteja ciente de que se você ativar essa opção, isso pode resultar em uma utilização de largura de banda substancialmente maior, pois a imagem ampliada deve ser carregada na sua totalidade, mesmo que nenhuma ação de zoom seja tomada pelo usuário. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
