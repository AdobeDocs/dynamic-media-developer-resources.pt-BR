---
title: op_colorize
description: Colorir imagem. Colore os dados da imagem, preservando sombras e realces.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# op_colorize{#op-colorize}

Colorir imagem. Colore os dados da imagem, preservando sombras e realces.

` op_colorize= *`cor`*[,off|norm[, *`contraste`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cor </span> </p> </td> 
  <td class="stentry"> <p>Cor do RGB de substituição. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">de </span> </p> </td> 
  <td class="stentry"> <p>Desabilitar compensação automática de brilho. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
  <td class="stentry"> <p>Habilitar compensação automática de brilho (padrão). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> Contraste </span> de <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Intervalo de contraste (0 a 100 reais); defina como 0 para preservar o contraste de entrada. </p> </td> 
 </tr> 
</table>

O segundo argumento especifica se o brilho da imagem de origem deve ser ajustado antes da coloração. Especifique `off` para desabilitar a compensação automática de brilho ou `norm` para ajustar o brilho automaticamente para que o valor mediano esteja com 50% de intensidade.

Defina o valor de *`contrast`* como 0 para preservar o intervalo de contraste da imagem de entrada ou especifique um intervalo de contraste desejado com um valor maior que 0. Um valor de 100 maximiza o contraste. Os valores típicos podem estar entre 30 e 70.

Além dos ajustes de brilho e contraste internos, `op_brightness=` e `op_contrast=` podem ser usados para ajustar ainda mais o efeito de coloração.

>[!NOTE]
>
>Os algoritmos de coloração usam apenas as informações de luminosidade nos dados da imagem. Essa conversão em tons de cinza é simples e não gerenciada por cores. `op_colorize` sempre gera dados de RGB, mesmo se a entrada estiver em tons de cinza ou CMYK.

## Propriedades {#section-c0f8bd424b864153a1108f384939f55b}

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. Ignorado pelas camadas de efeito.

*`color`* deve ser um valor RGB; não há suporte para valores *`color`* cinza ou CMYK.

O valor *`contrast`* será ignorado se a compensação de brilho estiver desativada.

Pressupõe-se que *`color`* exista no espaço de cores de trabalho correspondente ao tipo de pixel de *`color`*. *`color`* é convertido com precisão se a imagem da camada tiver um tipo de pixel diferente no momento da mesclagem.

Imagens CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, sem colorização. O segundo e o terceiro argumentos assumem o padrão `norm,0`, para compensação automática de brilho e sem alteração de contraste.

## Exemplo {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajustar dinamicamente o brilho e o contraste antes de colorir uma camada da imagem:

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Em vez disso, use o ajuste automático de brilho e contraste:

... `&op_colorize=a0b0c0,norm,50&`...

## Consulte também {#section-5581eb0e03014fa795e8f078c60e6c8d}

[cor](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gerenciamento de Cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
