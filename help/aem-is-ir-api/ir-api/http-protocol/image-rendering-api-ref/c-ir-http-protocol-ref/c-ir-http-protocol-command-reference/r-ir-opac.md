---
description: Opacidade. Especifica a opacidade do material.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 7910228217db2c97dccd306ce464c69da53ee576
workflow-type: tm+mt
source-wordcount: '112'
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

* Cor sólida e texturas repetíveis aplicadas a objetos de sobreposição textural.
* Materiais de revestimento de janelas aplicados a objetos de estrutura para revestimento de janelas.
* Decalhes aplicados a objetos textuais ou objetos de parede.

Se o material incluir uma imagem com um canal alfa, `opac=` poderá ser usado para tornar a imagem mais transparente, mas não mais opaca.

## Propriedades {#section-352f7b82ede54159b6afb90ae4b559ec}

Atributo de material. Ignorado se a seleção de objeto atual ou o material não suportar opacidade.

## Padrão {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, para um material totalmente opaco (se a imagem não incluir um canal alfa).
