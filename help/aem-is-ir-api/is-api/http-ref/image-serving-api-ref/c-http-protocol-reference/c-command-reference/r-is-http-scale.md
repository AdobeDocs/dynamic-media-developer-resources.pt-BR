---
title: escala
description: Dimensionar imagem. Dimensiona uma imagem de origem de camada por fator em relação à imagem com resolução total.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# escala{#scale}

Dimensionar imagem. Dimensiona uma imagem de origem de camada por fator em relação à imagem com resolução total.

`scale= *`fator`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fator</span> </p> </td> 
  <td class="stentry"> <p>Fator de escala (real, maior que 0,0). </p></td> 
 </tr> 
</table>

Nenhum dimensionamento é aplicado quando `scale=1`. *`factor`* menor que 1,0 diminui a escala e maior que 1,0 aumenta a imagem de origem.

## Propriedades {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Atributo de imagem/máscara de origem. Ignorado se `size=` também é especificada para a camada atual. Substituições `res=`. Aplica-se à camada 0, se especificada para `layer=comp`. Ignorado se a camada não estiver associada a uma imagem ou máscara.

## Padrão {#section-26e64904362342a5a62c5f6598f330c4}

Se não especificado, `res=` é usada. Se `res=` não for especificado, a imagem será usada sem dimensionamento.

## Consulte também {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
