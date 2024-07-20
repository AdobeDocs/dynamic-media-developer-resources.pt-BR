---
title: SpinView.maxloadradius
description: Representa o número máximo de quadros para pré-carregar em cada direção quando o SpinView está ocioso.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

Representa o número máximo de quadros para pré-carregar em cada direção quando o SpinView está ocioso.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valor</span></span> </p> </td> 
   <td colname="col2"> <p> Um valor de <span class="codeph"> -1</span> pré-carrega todos os quadros do conjunto. Os quadros pré-carregados são sempre vistos na resolução original de carregamento inicial do SpinView. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">ResAltos</span></span> </p> </td> 
   <td colname="col2"> <p> Controla a qualidade dos quadros pré-carregados. </p> <p>Quando definido como <span class="codeph"> 1</span>, os quadros são carregados em alta qualidade, correspondendo ao tamanho do componente. </p> <p>Quando definido como <span class="codeph"> 0</span>, somente o bloco de visualização de baixa resolução é carregado.</p> <p>O pré-carregamento em alta resolução melhora a experiência do usuário, especialmente quando a rotação automática está ativada. Ao mesmo tempo, isso resulta em um tempo de início mais lento e maior consumo de rede, portanto, deve ser usado com cuidado. Quando o carregamento prévio de alta resolução é usado, os quadros pré-carregados estarão sempre na resolução original na qual o componente foi carregado inicialmente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
