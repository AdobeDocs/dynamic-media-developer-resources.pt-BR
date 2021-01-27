---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic Media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Representa o número máximo de quadros a serem pré-carregados em cada direção quando o SpinView estiver ocioso. Um valor de <span class="codeph"> -1</span> pré-carrega todos os quadros no conjunto. Os quadros pré-carregados são sempre vistos na resolução original em que o SpinView foi carregado inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla a qualidade dos quadros pré-carregados. Quando definido como <span class="codeph"> 1</span> os quadros são carregados em alta qualidade, correspondendo ao tamanho do componente. Quando definido como <span class="codeph"> 0</span> apenas o bloco gráfico de pré-visualização de baixa resolução é carregado. </p> <p>O pré-carregamento em alta resolução melhora a experiência do usuário final, especialmente quando a rotação automática está ativada. Ao mesmo tempo, resulta em menor tempo de start e maior consumo de rede, portanto, use com cautela. Quando uma pré-carga de alta resolução é usada, os quadros pré-carregados estão sempre na resolução original na qual o componente foi inicialmente carregado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
