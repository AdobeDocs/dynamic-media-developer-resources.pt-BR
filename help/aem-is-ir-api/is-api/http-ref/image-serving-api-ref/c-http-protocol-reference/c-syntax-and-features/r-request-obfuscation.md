---
description: O conteúdo da parte inteira dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido pela aplicação da codificação base64 padrão.
solution: Experience Manager
title: Solicitar ofuscação
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Solicitar ofuscação{#request-obfuscation}

O conteúdo da parte inteira dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido pela aplicação da codificação base64 padrão.

O servidor tenta decodificar se `attribute::RequestObfuscation` está definido. Se a decodificação falhar, a solicitação será rejeitada. Se o bloqueio de solicitação e a ofuscação de solicitação forem aplicados, o sufixo de bloqueio deverá ser gerado e anexado antes da codificação base64.

>[!IMPORTANT]
>
>Se você ativar esse recurso, esteja ciente de que há certas limitações para seu uso que incluem o seguinte:<br>- A interface do usuário do Dynamic Media pode não mostrar os detalhes corretos para o **[!UICONTROL Last Published]** campo. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo HLS não funciona quando **[!UICONTROL Request obfuscation]** e **[!UICONTROL Request locking]** são ativados.<br>- Atualmente, alguns visualizadores do Dynamic Media não funcionam quando **[!UICONTROL Request obfuscation]** e **[!UICONTROL Request locking]** são ativados.

## Exemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica para:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Qualquer ocorrência de &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; em cadeias de caracteres de valor deve ser evitada com a codificação &#39;%xx&#39; antes de a solicitação ser ofuscada. Não é necessário codificar http de outra forma o *modificadores* parte da solicitação antes ou depois da ofuscação, mesmo se o bloqueio de solicitação for aplicado, já que a codificação base64 é segura para transmissão http.

## Consulte também {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificação HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Bloqueio de solicitação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
