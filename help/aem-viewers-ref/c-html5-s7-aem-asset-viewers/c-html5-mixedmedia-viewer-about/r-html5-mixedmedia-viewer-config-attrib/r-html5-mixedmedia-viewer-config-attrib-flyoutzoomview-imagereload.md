---
description: Configura como o componente busca novas imagens para a exibição principal e de flyout durante o redimensionamento.
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura como o componente busca novas imagens para a exibição principal e de flyout durante o redimensionamento.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largura de banda`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p>Quando definido como <span class="codeph"> 0 </span>, o componente não carrega novas imagens durante o redimensionamento, e a resolução da imagem na exibição do flyout não é alterada. </p> <p>Quando definido como <span class="codeph"> 1 </span> permite especificar um ou mais pontos de interrupção de largura para a imagem carregada na exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ponto de interrupção,  <span class="varname"> largura  </span>[;  <span class="varname"> largura  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>Pontos de interrupção de largura para a imagem carregada na exibição principal. O componente sempre usará o melhor tamanho de ajuste para a carga inicial. Após o redimensionamento, a imagem na exibição principal sempre será baixada com a largura igual ao ponto de interrupção maior mais próximo e baixada no cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
