---
title: rede
description: Saiba mais sobre como usar a otimização da largura de banda da rede para ajustar a qualidade da imagem fornecida com base na largura de banda real da rede.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# rede{#network}

Ativar a Largura de Banda da Rede ajusta automaticamente a qualidade da imagem fornecida com base na largura de banda real da rede. Para largura de banda de rede fraca, [DPR (Relação de pixels do dispositivo)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) a otimização é automaticamente desativada, mesmo que já esteja ativada.

Se desejar, sua empresa pode recusar a otimização da largura de banda da rede no nível da imagem individual anexando `network=off` ao URL da imagem.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ligado|desligado </span> </p> </td> 
  <td class="stentry"> <p>Especifica se a largura de banda de rede ajusta a qualidade da imagem fornecida com base na largura de banda de rede real (ativada) ou se a otimização da largura de banda de rede está desativada para nenhum ajuste de qualidade de imagem.</p> </td> 
 </tr> 
</table>

Os valores de DPR e largura de banda da rede são baseados nos valores detectados do lado do cliente do CDN empacotado. Esses valores às vezes são imprecisos. Por exemplo, iPhone5 com `dpr=2`e iPhone12 com `dpr=3`, ambos mostram `dpr=2`. Ainda, para dispositivos de alta resolução, enviar `dpr=2` é melhor do que enviar dpr=1. No entanto, a melhor maneira de superar essa imprecisão é usar a DPR do lado do cliente para fornecer valores 100% precisos. E funciona para qualquer dispositivo, seja Apple ou qualquer outro dispositivo que tenha sido iniciado. Consulte [Usar Imagem inteligente com proporção de pixels do dispositivo no lado do cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Propriedades



## Padrão

`network=off`

## Exemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Consulte também

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Imagem inteligente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)