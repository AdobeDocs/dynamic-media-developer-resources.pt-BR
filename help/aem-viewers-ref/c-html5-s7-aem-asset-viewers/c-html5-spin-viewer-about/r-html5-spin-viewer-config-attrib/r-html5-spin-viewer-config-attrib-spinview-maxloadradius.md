---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Developer,Business Practitioner
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valueHighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Representa o número máximo de quadros para pré-carregar em cada direção quando o SpinView estiver inativo. Um valor de <span class="codeph"> -1</span> pré-carrega todos os quadros no conjunto. Os quadros pré-carregados são sempre vistos na resolução original de que o SpinView foi inicialmente carregado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla a qualidade dos quadros pré-carregados. Quando definido como <span class="codeph"> 1</span> os quadros são carregados em alta qualidade, correspondendo ao tamanho do componente. Quando definido como <span class="codeph"> 0</span> somente o bloco de visualização de baixa resolução é carregado. </p> <p>O pré-carregamento em alta resolução melhora a experiência do usuário final, especialmente quando a rotação automática está ativada. Ao mesmo tempo, resulta em tempo de início mais lento e maior consumo de rede, portanto, use com cautela. Quando um pré-carregamento de alta resolução é usado, os quadros pré-carregados sempre estão na resolução original em que o componente foi carregado inicialmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
