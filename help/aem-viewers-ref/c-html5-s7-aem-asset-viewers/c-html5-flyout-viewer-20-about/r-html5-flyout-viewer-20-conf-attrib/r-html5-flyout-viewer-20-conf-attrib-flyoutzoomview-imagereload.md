---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic Media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`largura de `*[; *`largura`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Configura como o componente obtém novas imagens para a visualização principal e flyout durante o redimensionamento. </p> <p>Quando definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento; a resolução da imagem na visualização do flyout não é alterada. </p> <p>A configuração para <span class="codeph"> 1 </span> permite que você especifique um ou mais pontos de interrupção de largura para a imagem carregada na visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ponto de interrupção,  <span class="varname"> largura  </span>[;  <span class="varname"> largura  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> Pontos de interrupção de largura para a imagem carregada na visualização principal. O componente sempre usa o melhor tamanho de ajuste para a carga inicial. Após o redimensionamento, garante que a imagem na visualização principal seja sempre baixada com a largura igual ao ponto de interrupção maior mais próximo e baixada no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
