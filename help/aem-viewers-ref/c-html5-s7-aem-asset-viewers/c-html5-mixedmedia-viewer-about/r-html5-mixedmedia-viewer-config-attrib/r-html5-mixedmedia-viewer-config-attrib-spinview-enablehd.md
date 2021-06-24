---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Developer,Business Practitioner
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Ative, limite ou desative a otimização para dispositivos em que <span class="codeph"> devicePixelRatio</span> é maior que <span class="codeph"> 1</span>, ou seja, dispositivos com uma exibição de alta densidade como o iPhone4 e dispositivos semelhantes. Se estiver ativo, o componente limita o tamanho da solicitação de imagem IS como se o dispositivo tivesse apenas uma proporção de pixel de <span class="codeph"> 1</span> e, portanto, reduz a largura de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Se estiver usando a configuração <span class="codeph"> limit</span>, o componente ativará a alta densidade de pixels somente até o limite especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
