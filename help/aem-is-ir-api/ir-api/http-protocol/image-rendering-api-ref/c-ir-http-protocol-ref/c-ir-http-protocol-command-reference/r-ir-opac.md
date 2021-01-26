---
description: Opacidade. Especifica a opacidade do material.
seo-description: Opacidade. Especifica a opacidade do material.
seo-title: opaco
solution: Experience Manager
title: opaco
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# opac{#opac}

Opacidade. Especifica a opacidade do material.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Opacidade do material (percentagem); 0...100 </p> </td> 
 </tr> 
</table>

As seguintes combinações de material/objeto oferecem suporte para a opacidade da variável:

* A cor sólida e as texturas repetíveis aplicadas a objetos de sobreposição texturizáveis.
* Materiais de revestimento de janelas aplicados a objetos de armação de revestimento de janelas.
* Decretos aplicados a objetos texturizáveis ou objetos de parede.

Se o material incluir uma imagem com um canal alfa, `opac=` poderá ser usado para tornar a imagem mais transparente, mas não mais opaca.

## Propriedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo material. Ignorado se a seleção de objeto atual ou o material não suportar opacidade.

## Padrão {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para um material totalmente opaco (se a imagem não incluir um canal alfa).
