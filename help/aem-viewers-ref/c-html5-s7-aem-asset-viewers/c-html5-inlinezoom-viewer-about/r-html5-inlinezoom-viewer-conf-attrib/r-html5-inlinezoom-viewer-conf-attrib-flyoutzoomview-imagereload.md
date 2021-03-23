---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largura de banda`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Configura como o componente busca novas imagens para a exibição principal e de flyout durante o redimensionamento. </p> <p>Definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento e a resolução da imagem na exibição do flyout não é alterada. </p> <p>Definir como <span class="codeph"> 1 </span> permite especificar um ou mais pontos de interrupção de largura para a imagem carregada na exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ponto de interrupção,  <span class="varname"> largura  </span>;  <span class="varname"> largura  </span> </span> </p> </td> 
   <td colname="col2"> <p>Pontos de interrupção de largura para a imagem carregada na exibição principal. </p> <p>O componente sempre usa o tamanho de melhor ajuste para a carga inicial. Após o redimensionamento, a imagem na exibição principal sempre será baixada usando a largura igual ao ponto de interrupção maior mais próximo e baixada no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
