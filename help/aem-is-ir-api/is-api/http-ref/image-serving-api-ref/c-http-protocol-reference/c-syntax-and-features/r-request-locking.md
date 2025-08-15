---
description: Para reduzir a oportunidade de adulteração de solicitações, é fornecido um simples recurso de bloqueio.
solution: Experience Manager
title: Bloqueio de solicitação
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Bloqueio de solicitação{#request-locking}

Para reduzir a oportunidade de adulteração de solicitações, é fornecido um simples recurso de bloqueio.

Se attribute::RequestLock estiver definido, um valor de bloqueio deverá ser anexado à solicitação no formato `&xxxx`, com xxxx sendo um valor hexadecimal de quatro dígitos. Este valor hexadecimal é gerado usando um algoritmo de hash simples aplicado à parte *modificadores* da solicitação (após &#39;?&#39; que separa o caminho da URL dos *modificadores*). Isso deve ser feito depois que a solicitação é totalmente codificada em http, mas antes de ser ofuscada (opcionalmente). Depois de desofuscar a solicitação, o servidor usa o mesmo algoritmo de hash na string do modificador (excluindo os últimos 5 caracteres, que contêm o valor lock). Se a chave gerada não corresponder ao bloqueio, a solicitação será rejeitada.

>[!IMPORTANT]
>
>Se você habilitar esse recurso, esteja ciente de que há certas limitações para seu uso que incluem o seguinte:<br>- A interface de usuário do Dynamic Media pode não mostrar os detalhes corretos para o campo **[!UICONTROL Last Published]**. No entanto, esse efeito não afeta a publicação.<br>- Atualmente, o streaming de vídeo do HLS não funciona quando o **[!UICONTROL Request obfuscation]** e o **[!UICONTROL Request locking]** estão habilitados.<br>- Atualmente, alguns Visualizadores do Dynamic Media não funcionam quando o **[!UICONTROL Request obfuscation]** e o **[!UICONTROL Request locking]** estão habilitados.

Código de amostra do C++ para gerar o valor de bloqueio da solicitação:

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

[Codificação HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Solicitar Ofuscação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
