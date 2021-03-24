---
description: Região de interesse. Especifica uma região retangular de interesse (ROI) na imagem composta, expressa em pixels.
solution: Experience Manager
title: gn
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# rgn{#rgn}

Região de interesse. Especifica uma região retangular de interesse (ROI) na imagem composta, expressa em pixels.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cabo</span> </p> </td> 
  <td class="stentry"> <p>Deslocamento de pixels do canto superior esquerdo da imagem composta para o canto superior esquerdo do ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Tamanho do ROI em pixels (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` O define somente um ROI sem cortar a imagem. Quando `wid=` e/ou `hei=` maior que o tamanho também são aplicados, dados adicionais da imagem composta podem ser visíveis na imagem de resposta final.

## Propriedades {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Exibir atributo. Aplica-se independentemente da configuração de camada atual.

Qualquer área do ROI que se estende fora da imagem composta é preenchida com `bgc=`.

`rgn=` é aplicada antes da escala final e ajuste com  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=` ou  `align=`.

## Padrão {#section-6a3df8f670084def900ffef9dab7e94a}

Imagem composta inteira ( `rgn=0,0,width,height`).

## Consulte também {#section-07883760f25c4d17aedbee36b7883891}

[cortar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [alinhar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [ajustar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
