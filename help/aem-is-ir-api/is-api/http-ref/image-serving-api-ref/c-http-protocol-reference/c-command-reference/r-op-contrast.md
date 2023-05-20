---
description: Ajuste o contraste. Ajusta o contraste da imagem aumentando o brilho dos pixels com mais de 50% de brilho e reduzindo o brilho dos pixels com menos de 50% de brilho.
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# op_contrast{#op-contrast}

Ajuste o contraste. Ajusta o contraste da imagem aumentando o brilho dos pixels com mais de 50% de brilho e reduzindo o brilho dos pixels com menos de 50% de brilho.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de contraste em porcentagem (-100...100 int). </p></td> 
 </tr> 
</table>

## Propriedades {#section-d319ed55057344eab0a3c93f720acdbf}

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, para que não haja alteração no contraste. Imagens CMYK ou camadas são convertidas em RGB antes da operação ser aplicada.

## Exemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Diminua o contraste e a nitidez de uma camada de imagem de maior qualidade para combiná-la visualmente a uma foto de fundo de baixa qualidade:

… `&op_blur=3&op_contrast=-12&`

Uma versão futura pode usar o brilho mediano da imagem em vez de um brilho fixo de 50%.
