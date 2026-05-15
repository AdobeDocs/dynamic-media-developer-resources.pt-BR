---
description: O conteúdo da parte inteira dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido pela aplicação da codificação base64 padrão.
solution: Experience Manager
title: Solicitar ofuscação
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Solicitar ofuscação{#request-obfuscation}

O conteúdo da parte inteira dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido pela aplicação da codificação base64 padrão.

O servidor tentará decodificar se `attribute::RequestObfuscation` estiver definido. Se a decodificação falhar, a solicitação será rejeitada. Se o bloqueio de solicitação e a ofuscação de solicitação forem aplicados, o sufixo de bloqueio deverá ser gerado e anexado antes da codificação base64.

>[!IMPORTANT]
>
>Se você habilitar esse recurso, esteja ciente de que há certas limitações para seu uso que incluem o seguinte:<br>- A interface de usuário do Dynamic Media pode não mostrar os detalhes corretos para o campo **[!UICONTROL Last Published]**. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo do HLS não funciona quando o **[!UICONTROL Request obfuscation]** e o **[!UICONTROL Request locking]** estão habilitados.<br>- Atualmente, alguns Visualizadores do Dynamic Media não funcionam quando o **[!UICONTROL Request obfuscation]** e o **[!UICONTROL Request locking]** estão habilitados.

## Exemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica para:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Qualquer ocorrência de &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; em cadeias de caracteres de valor deve ser evitada com a codificação &#39;%xx&#39; antes de a solicitação ser ofuscada. Não é necessário codificar http na parte *modifiers* da solicitação antes ou depois da ofuscação, mesmo se o bloqueio de solicitação for aplicado, pois a codificação base64 é segura para transmissão http.

## Consulte também {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificação HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Solicitar Bloqueio](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
