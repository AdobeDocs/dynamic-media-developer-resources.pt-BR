---
description: Ajuste a matiz. Alterna a matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.
seo-description: Ajuste a matiz. Alterna a matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# op_hue{#op-hue}

Ajuste a matiz. Alterna a matiz de cada pixel visível da camada ou imagem composta pela quantidade especificada.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de matiz em graus (-180...+180 int). </p></td> 
 </tr> 
</table>

Baseado em um intervalo de matiz de 360 graus.

## Propriedades {#section-55779644700b4c808a624cdf5a04447e}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito. As imagens ou camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, sem qualquer alteração na matiz.
