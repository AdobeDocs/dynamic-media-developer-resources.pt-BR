---
description: Ajuste o contraste. Ajusta o contraste da imagem aumentando o brilho dos pixels com mais de 50% de brilho e reduzindo o brilho dos pixels com menos de 50% de brilho.
seo-description: Ajuste o contraste. Ajusta o contraste da imagem aumentando o brilho dos pixels com mais de 50% de brilho e reduzindo o brilho dos pixels com menos de 50% de brilho.
seo-title: op_Contraste
solution: Experience Manager
title: op_Contraste
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# op_Contraste{#op-contrast}

Ajuste o contraste. Ajusta o contraste da imagem aumentando o brilho dos pixels com mais de 50% de brilho e reduzindo o brilho dos pixels com menos de 50% de brilho.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de contraste em porcentagem (-100...100 int). </p></td> 
 </tr> 
</table>

## Propriedades {#section-d319ed55057344eab0a3c93f720acdbf}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, para que não haja mudança no contraste. As imagens ou camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Exemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Diminua o contraste e a nitidez de uma camada de imagem de qualidade superior para equipará-la visualmente a uma foto de fundo de baixa qualidade:

... `&op_blur=3&op_contrast=-12&`

Uma versão futura pode usar o brilho mediano da imagem em vez de um brilho fixo de 50%.
