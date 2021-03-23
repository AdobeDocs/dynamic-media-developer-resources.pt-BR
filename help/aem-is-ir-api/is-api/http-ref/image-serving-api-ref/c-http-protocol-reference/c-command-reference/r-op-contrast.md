---
description: Ajuste o contraste. Ajusta o contraste da imagem, aumentando o brilho dos pixels com mais de 50% de brilho, e reduzindo o brilho dos pixels com menos de 50% de brilho.
seo-description: Ajuste o contraste. Ajusta o contraste da imagem, aumentando o brilho dos pixels com mais de 50% de brilho, e reduzindo o brilho dos pixels com menos de 50% de brilho.
seo-title: op_contraste
solution: Experience Manager
title: op_contraste
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# op_contraste{#op-contrast}

Ajuste o contraste. Ajusta o contraste da imagem, aumentando o brilho dos pixels com mais de 50% de brilho, e reduzindo o brilho dos pixels com menos de 50% de brilho.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de contraste em porcentagem (-100...100 int). </p></td> 
 </tr> 
</table>

## Propriedades {#section-d319ed55057344eab0a3c93f720acdbf}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito.

## Padrão {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, sem alterações no contraste. Imagens ou camadas CMYK são convertidas em RGB antes da aplicação da operação.

## Exemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Diminua o contraste e a nitidez de uma camada de imagem de maior qualidade para combiná-la visualmente a uma foto de fundo de baixa qualidade:

... `&op_blur=3&op_contrast=-12&`

Uma versão futura pode usar o brilho mediano da imagem em vez de um brilho fixo de 50%.
