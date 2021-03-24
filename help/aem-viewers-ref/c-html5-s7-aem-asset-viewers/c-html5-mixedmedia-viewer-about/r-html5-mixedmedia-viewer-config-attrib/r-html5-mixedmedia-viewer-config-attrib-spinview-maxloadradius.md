---
description: Representa o número máximo de quadros para pré-carregar em cada direção quando o SpinView estiver inativo.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Representa o número máximo de quadros para pré-carregar em cada direção quando o SpinView estiver inativo.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valueHighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Um valor de <span class="codeph"> -1</span> pré-carrega todos os quadros no conjunto. Os quadros pré-carregados são sempre vistos na resolução original de que o SpinView foi inicialmente carregado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controla a qualidade dos quadros pré-carregados. </p> <p>Quando definido como <span class="codeph"> 1</span> os quadros são carregados em alta qualidade, correspondendo ao tamanho do componente. </p> <p>Quando definido como <span class="codeph"> 0</span> somente o bloco de visualização de baixa resolução é carregado. </p> <p>O pré-carregamento em alta resolução melhora a experiência do usuário final, especialmente quando a rotação automática está ativada. Ao mesmo tempo, resulta em tempo de início mais lento e maior consumo de rede, portanto, deve ser usado com cuidado. Quando é usado o pré-carregamento de alta resolução, os quadros pré-carregados ficam sempre na resolução original na qual o componente foi inicialmente carregado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
