---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`largura`*[; *`largura`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configura como o componente busca novas imagens para a exibição principal e de imagem suspensa durante o redimensionamento. </p> <p>Definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento e a resolução da imagem na exibição da imagem suspensa não é alterada. </p> <p>Definir como <span class="codeph"> 1 </span> permite que você especifique um ou mais pontos de interrupção de largura para a imagem carregada na exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ponto de interrupção <span class="codeph">, <span class="varname"> largura </span>; <span class="varname"> largura </span> </span> </p> </td> 
   <td colname="col2"> <p>Pontos de interrupção de largura da imagem carregada na exibição principal. </p> <p>O componente sempre usa o melhor tamanho para a carga inicial. Após o redimensionamento, ele garante que a imagem na exibição principal sempre seja baixada com a largura igual ao ponto de interrupção maior mais próximo e seja reduzida no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
