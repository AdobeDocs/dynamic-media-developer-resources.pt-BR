---
title: op_hue
description: Ajuste a matiz. Desloca o matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# op_hue{#op-hue}

Ajuste a matiz. Desloca o matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de matiz em graus (-180...+180 int). </p></td> 
 </tr> 
</table>

Baseado em um intervalo de matiz de 360 graus.

## Propriedades {#section-55779644700b4c808a624cdf5a04447e}

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito. Imagens CMYK ou camadas são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, para não alterar o matiz.
