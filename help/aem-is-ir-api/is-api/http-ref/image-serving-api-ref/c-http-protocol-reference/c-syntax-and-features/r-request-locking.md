---
description: Para reduzir a possibilidade de adulteração de pedidos, é disponibilizada uma facilidade de bloqueio simples.
seo-description: Para reduzir a possibilidade de adulteração de pedidos, é disponibilizada uma facilidade de bloqueio simples.
seo-title: Bloqueio de solicitação
solution: Experience Manager
title: Bloqueio de solicitação
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Solicitar bloqueio{#request-locking}

Para reduzir a possibilidade de adulteração de pedidos, é disponibilizada uma facilidade de bloqueio simples.

Se o atributo::RequestLock estiver definido, um valor de bloqueio deve ser anexado à solicitação, na forma de `&xxxx`, com xxxx sendo um valor hexadecimal de quatro dígitos. Esse valor hexadecimal é gerado usando um algoritmo hex simples aplicado à parte *modifiers* da solicitação (após &#39;?&#39; que separa o caminho do URL dos *modificadores*). Isso deve ser feito depois que a solicitação for totalmente codificada em http, mas antes que seja (opcionalmente) ofuscada. Depois de desofuscar a solicitação, o servidor usará o mesmo algoritmo de hash na string do modificador (excluindo os últimos 5 caracteres, que contêm o valor de bloqueio). Se a chave gerada não corresponder ao bloqueio, a solicitação será rejeitada.

>[!IMPORTANT]
>
>Se ativar este recurso, esteja ciente de que existem certas limitações ao seu uso que incluem o seguinte:<br>- A interface do usuário do Dynamic Media pode não mostrar os detalhes corretos para o campo **[!UICONTROL Last Published]**. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo HLS não funciona quando **[!UICONTROL Request obfuscation]** e  **[!UICONTROL Request locking]** são ativados.<br>- Atualmente, alguns visualizadores do Dynamic Media não funcionam quando  **[!UICONTROL Request obfuscation]** e  **[!UICONTROL Request locking]** são ativados.

Código de amostra C++ para gerar o valor de bloqueio de solicitação:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Consulte também {#section-a6d45406c0354669ac581793e4fa8436}

[Codificação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP, Ofuscação  [de solicitação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [atributo::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
