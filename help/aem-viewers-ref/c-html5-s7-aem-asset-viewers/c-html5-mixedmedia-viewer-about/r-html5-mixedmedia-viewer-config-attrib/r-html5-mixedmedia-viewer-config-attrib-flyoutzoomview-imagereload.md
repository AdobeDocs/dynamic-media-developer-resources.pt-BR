---
title: FlyoutZoomView.imagereload
description: Configura como o componente busca novas imagens para a exibição principal e de imagem suspensa durante o redimensionamento.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura como o componente busca novas imagens para a exibição principal e de imagem suspensa durante o redimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`largura`*[; *`largura`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Quando definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento e a resolução de imagem na exibição da imagem suspensa não é alterada. </p> <p>Quando definido como <span class="codeph"> 1 </span> permite que você especifique um ou mais pontos de interrupção de largura para a imagem carregada na exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ponto de interrupção <span class="codeph">, <span class="varname"> largura </span>[; <span class="varname"> largura </span>] </span> </p> </td> 
   <td colname="col2"> <p>Pontos de interrupção de largura da imagem carregada na exibição principal. O componente sempre usa o melhor tamanho para a carga inicial. Depois do redimensionamento, garante que a imagem na exibição principal seja sempre baixada com largura igual ao maior ponto de interrupção mais próximo e reduzida no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
