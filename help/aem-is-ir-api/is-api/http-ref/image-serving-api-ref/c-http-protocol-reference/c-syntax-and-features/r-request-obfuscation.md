---
description: O conteúdo de toda a parte dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser ocultado pela aplicação da codificação padrão base64.
seo-description: O conteúdo de toda a parte dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser ocultado pela aplicação da codificação padrão base64.
seo-title: Ofuscação de solicitação
solution: Experience Manager
title: Ofuscação de solicitação
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 80ae3a549340156bb74faa1793c43d3a8fa3853c
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Ofuscação de solicitação{#request-obfuscation}

O conteúdo de toda a parte dos modificadores da string de solicitação, incluindo o sufixo de bloqueio opcional, pode ser ocultado pela aplicação da codificação padrão base64.

O servidor tentará decodificar se `attribute::RequestObfuscation` estiver definido. Se a decodificação falhar, o pedido será rejeitado. Se o bloqueio de solicitação e a ofuscação de solicitação forem aplicados, o sufixo de bloqueio deverá ser gerado e anexado antes da codificação de base64.

>[!IMPORTANT]
>
>Se você habilitar esse recurso, esteja ciente de que há certas limitações ao seu uso que incluem o seguinte:<br>- A interface do usuário do Dynamic Media pode não mostrar os detalhes corretos para o **[!UICONTROL Last Published]** campo. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo HLS não funciona quando **[!UICONTROL Request obfuscation]** e **[!UICONTROL Request locking]** são ativados.

## Example {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica para:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Quaisquer ocorrências de &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; em sequências de caracteres de valor devem ser evitadas usando a codificação &#39;%xx&#39;, antes que a solicitação seja ofuscada. Caso contrário, não é necessário codificar http-encodecer a parte dos *modificadores* da solicitação antes ou depois da ofuscação, mesmo se o bloqueio da solicitação for aplicado, já que a codificação base64 é segura para transmissão http.

## Consulte também {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codificação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)HTTP, Bloqueio [de](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)solicitação, [atributo::RequestOfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
