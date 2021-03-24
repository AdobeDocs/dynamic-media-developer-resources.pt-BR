---
description: Ajustar matiz. Alterna o matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# op_hue{#op-hue}

Ajustar matiz. Alterna o matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de matiz em graus (-180...+180 int). </p></td> 
 </tr> 
</table>

Baseado em um intervalo de matiz de 360 graus.

## Propriedades {#section-55779644700b4c808a624cdf5a04447e}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito. Imagens ou camadas CMYK são convertidas em RGB antes da aplicação da operação.

## Padrão {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sem alterações na matiz.
