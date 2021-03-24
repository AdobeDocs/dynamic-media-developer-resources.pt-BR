---
description: Dimensionar imagem. Dimensiona uma imagem de origem de camada por fator em relação à imagem de resolução completa.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# scale{#scale}

Dimensionar imagem. Dimensiona uma imagem de origem de camada por fator em relação à imagem de resolução completa.

`scale= *`fator`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fator</span> </p> </td> 
  <td class="stentry"> <p>Fator de escala (real, maior que 0,0). </p></td> 
 </tr> 
</table>

Nenhum dimensionamento é aplicado quando `scale=1`. *`factor`* menor que 1,0 escala baixa e maior que 1,0 amplia a imagem de origem.

## Propriedades {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Imagem de origem/atributo de máscara. Ignorado se `size=` também for especificado para a camada atual. Substitui `res=`. Aplica-se à camada 0, se especificado para `layer=comp`. Ignorado se a camada não estiver associada a uma imagem ou máscara.

## Padrão {#section-26e64904362342a5a62c5f6598f330c4}

Se não especificado, `res=` é usado. Se `res=` não for especificado, a imagem será usada sem dimensionamento.

## Consulte também {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [tamanho=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
