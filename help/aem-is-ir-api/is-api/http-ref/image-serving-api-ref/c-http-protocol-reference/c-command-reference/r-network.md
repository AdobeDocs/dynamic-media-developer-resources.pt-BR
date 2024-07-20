---
title: rede
description: Saiba mais sobre como usar a otimização da largura de banda da rede para ajustar a qualidade da imagem fornecida com base na largura de banda real da rede.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# rede{#network}

Ativar a Largura de Banda da Rede ajusta automaticamente a qualidade da imagem fornecida com base na largura de banda real da rede. Para largura de banda de rede insuficiente, a otimização de [DPR (Relação de Pixels do Dispositivo)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) é automaticamente desativada, mesmo que já esteja ativada.

Se desejar, sua empresa pode recusar a otimização da largura de banda da rede no nível da imagem individual, anexando `network=off` à URL da imagem.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ligado|desligado </span> </p> </td> 
  <td class="stentry"> <p>Especifica se a largura de banda de rede ajusta a qualidade da imagem fornecida com base na largura de banda de rede real (ativada) ou se a otimização da largura de banda de rede está desativada para nenhum ajuste de qualidade de imagem.</p> </td> 
 </tr> 
</table>

Os valores de largura de banda da rede são baseados nos valores detectados do lado do cliente do CDN agrupado.

## Propriedades

Um atributo de solicitação. Não tem efeito se as condições da rede forem excelentes.

## Padrão

`network=off`

## Exemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Consulte também

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
