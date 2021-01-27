---
description: Representa o número máximo de quadros a serem pré-carregados em cada direção quando o SpinView estiver ocioso.
seo-description: Representa o número máximo de quadros a serem pré-carregados em cada direção quando o SpinView estiver ocioso.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic Media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Representa o número máximo de quadros a serem pré-carregados em cada direção quando o SpinView estiver ocioso.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Um valor de <span class="codeph"> -1</span> pré-carrega todos os quadros no conjunto. Os quadros pré-carregados são sempre vistos na resolução original em que o SpinView foi carregado inicialmente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla a qualidade dos quadros pré-carregados. </p> <p>Quando definido como <span class="codeph"> 1</span>, os quadros são carregados em alta qualidade, correspondendo ao tamanho do componente. </p> <p>Quando definido como <span class="codeph"> 0</span> apenas o bloco gráfico de pré-visualização de baixa resolução é carregado. </p> <p>O pré-carregamento em alta resolução melhora a experiência do usuário final, especialmente quando a rotação automática está ativada. Ao mesmo tempo, resulta em um tempo de start mais lento e maior consumo de rede, portanto, deve ser usado com cuidado. Quando a pré-carga de alta resolução é usada, os quadros pré-carregados estão sempre na resolução original na qual o componente foi carregado inicialmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
