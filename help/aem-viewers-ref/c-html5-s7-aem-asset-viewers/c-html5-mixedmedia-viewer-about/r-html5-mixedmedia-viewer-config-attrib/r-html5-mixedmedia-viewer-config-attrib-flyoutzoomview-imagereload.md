---
description: Configura como o componente obtém novas imagens para a visualização principal e flyout durante o redimensionamento.
seo-description: Configura como o componente obtém novas imagens para a visualização principal e flyout durante o redimensionamento.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic Media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura como o componente obtém novas imagens para a visualização principal e flyout durante o redimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`largura de `*[; *`largura`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p>Quando definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento, e a resolução da imagem na visualização flyout não é alterada. </p> <p>Quando definido como <span class="codeph"> 1 </span> permite que você especifique um ou mais pontos de interrupção de largura para a imagem carregada na visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ponto de interrupção,  <span class="varname"> largura  </span>[;  <span class="varname"> largura  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>Pontos de interrupção de largura para a imagem carregada na visualização principal. O componente sempre usará o melhor tamanho de ajuste para a carga inicial. Após o redimensionamento, a imagem na visualização principal sempre será baixada com a largura igual ao ponto de interrupção maior mais próximo e baixada no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
