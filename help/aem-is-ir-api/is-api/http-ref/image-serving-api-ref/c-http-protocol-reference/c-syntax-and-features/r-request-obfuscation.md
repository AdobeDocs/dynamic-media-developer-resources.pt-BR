---
description: O conteúdo de toda a parte dos modificadores da cadeia de caracteres de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido ao aplicar a codificação padrão base64.
solution: Experience Manager
title: Ofuscação de solicitação
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Ofuscação de solicitação{#request-obfuscation}

O conteúdo de toda a parte dos modificadores da cadeia de caracteres de solicitação, incluindo o sufixo de bloqueio opcional, pode ser obscurecido ao aplicar a codificação padrão base64.

O servidor tenta decodificar se `attribute::RequestObfuscation` estiver definido. Se a decodificação falhar, a solicitação será rejeitada. Se o bloqueio de solicitação e a ofuscação de solicitação forem aplicados, o sufixo de bloqueio deverá ser gerado e anexado antes da codificação base64.

>[!IMPORTANT]
>
>Se você habilitar esse recurso, esteja ciente de que há certas limitações para seu uso que incluem o seguinte:<br>- A interface do usuário do Dynamic Media pode não mostrar os detalhes corretos para o campo **[!UICONTROL Last Published]**. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo HLS não funciona quando **[!UICONTROL Request obfuscation]** e  **[!UICONTROL Request locking]** são ativados.<br>- Atualmente, alguns visualizadores do Dynamic Media não funcionam quando  **[!UICONTROL Request obfuscation]** e  **[!UICONTROL Request locking]** são ativados.

## Exemplo {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica para:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Qualquer ocorrência de &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; em sequências de valores deve ser escapada usando a codificação &#39;%xx&#39;, antes que a solicitação seja ofuscada. Não é necessário codificar http-encode a parte *modifiers* da solicitação antes ou depois da ofuscação, mesmo se o bloqueio de solicitação for aplicado, já que a codificação base64 é segura para transmissão http.

## Consulte também {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, Bloqueio de  [solicitação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [atributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
