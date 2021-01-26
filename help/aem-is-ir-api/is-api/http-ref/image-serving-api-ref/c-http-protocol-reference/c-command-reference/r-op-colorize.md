---
description: Colorir imagem. Colora os dados da imagem enquanto preserva sombras e realces.
seo-description: Colorir imagem. Colora os dados da imagem enquanto preserva sombras e realces.
seo-title: op_colorizar
solution: Experience Manager
title: op_colorizar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# op_colorize{#op-colorize}

Colorir imagem. Colora os dados da imagem enquanto preserva sombras e realces.

` op_colorize= *`contraste `*[,off|norm[, *`colorido`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cor  </span> </p> </td> 
  <td class="stentry"> <p>Cor RGB de substituição. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> off  </span> </p> </td> 
  <td class="stentry"> <p>Desative a compensação automática de brilho. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma  </span> </p> </td> 
  <td class="stentry"> <p>Ative a compensação automática de brilho (padrão). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contraste  </span> </p> </td> 
  <td class="stentry"> <p>Intervalo de contraste (real 0,100); defina para 0 para preservar o contraste de entrada. </p> </td> 
 </tr> 
</table>

O segundo argumento especifica se o brilho da imagem de origem deve ser ajustado antes de colorir. Especifique `off` para desativar a compensação automática de brilho ou `norm` para ajustar o brilho automaticamente, de modo que o valor médio esteja na intensidade de 50%.

Defina o valor *`contrast`* como 0 para preservar o intervalo de contraste da imagem de entrada, ou especifique um intervalo de contraste desejado com um valor maior que 0. Um valor de 100 maximiza o contraste. Valores típicos podem estar entre 30 e 70.

Além dos ajustes integrados de brilho e contraste, `op_brightness=` e `op_contrast=` podem ser usados para ajustar ainda mais o efeito de colorização.

>[!NOTE]
>
>O algoritmo de colorização usa apenas as informações de luminância nos dados da imagem. Essa conversão em tons de cinza é simples e não gerenciada por cores. `op_colorize` sempre gera dados RGB, mesmo se a entrada for em tons de cinza ou CMYK.

## Propriedades {#section-c0f8bd424b864153a1108f384939f55b}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito.

*`color`* deve ser um valor RGB; não há suporte para  *`color`* valores cinza ou CMYK.

O valor *`contrast`* será ignorado se a compensação de brilho estiver desativada.

*`color`* presume-se que existe no espaço de cor de trabalho correspondente ao tipo de pixel de  *`color`*. *`color`* é convertida com precisão se a imagem da camada tiver um tipo de pixel diferente no momento da mesclagem.

As imagens CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, sem colorização. O segundo e o terceiro argumentos assumem `norm,0` como padrão, para compensação automática de brilho e sem alteração de contraste.

## Exemplo {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajuste o brilho e o contraste dinamicamente antes de colorir uma camada de imagem:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Em vez disso, use o ajuste automático de brilho e contraste:

... `&op_colorize=a0b0c0,norm,50&`...

## Consulte também {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_Contraste=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), Gerenciamento  [de cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
