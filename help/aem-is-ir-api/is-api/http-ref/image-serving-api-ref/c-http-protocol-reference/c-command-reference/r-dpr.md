---
title: dpr
description: Proporção de pixels do dispositivo (DPR)&mdash;também conhecida como Proporção de pixels CSS&mdash;é a relação entre os pixels físicos e os pixels lógicos de um dispositivo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 21d6aed6baee24922732461fe680f6cc93bd0d06
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# dpr{#dpr}

A Relação de pixels do dispositivo (DPR), também conhecida como Relação de pixels CSS, é a relação entre os pixels físicos e os pixels lógicos de um dispositivo. Especialmente com o advento das telas retina, a resolução de pixels de dispositivos móveis modernos está crescendo a uma taxa rápida.

Ativar a otimização da Proporção de pixels do dispositivo renderiza a imagem na resolução nativa da tela, o que a torna nítida.

Atualmente, a densidade de pixels da exibição vem dos valores de cabeçalho da CDN Akamai.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> desligado </span> </span> </p> </td> 
  <td class="stentry"> <p>Desative a otimização de DPR em um nível de URL de imagem individual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ativado, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Substitua o valor do DPR detectado pelo Smart Imaging, com um valor personalizado (conforme detectado por qualquer lógica do lado do cliente ou por outros meios). O valor permitido para dprValue é qualquer número maior que 0. </p> </td> 
 </tr> 
</table>


Você pode usar `dpr=on,dprValue` mesmo que a configuração da DPR no nível da empresa esteja desativada.

Devido à otimização da DPR, quando a imagem resultante é maior que a configuração MaxPix Dynamic Media, a largura MaxPix é sempre reconhecida ao manter a proporção da imagem.

| Tamanho da imagem solicitada | Valor de DPR | Tamanho da imagem entregue |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

Os valores de DPR são baseados nos valores detectados do lado do cliente do CDN agrupado. Esses valores às vezes são imprecisos. Por exemplo, iPhone5 com `dpr=2`e iPhone12 com dpr=3, ambos mostram `dpr=2`. Ainda, para dispositivos de alta resolução, enviar `dpr=2` é melhor do que enviar `dpr=1`. No entanto, a melhor maneira de superar essa imprecisão é usar a DPR do lado do cliente para fornecer valores 100% precisos. E funciona para qualquer dispositivo, seja Apple ou qualquer outro dispositivo que tenha sido iniciado. Consulte [Usar Imagem inteligente com proporção de pixels do dispositivo no lado do cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Propriedades



## Padrão

`dpr=off`


## Exemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Consulte também

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [rede](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imagem inteligente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)