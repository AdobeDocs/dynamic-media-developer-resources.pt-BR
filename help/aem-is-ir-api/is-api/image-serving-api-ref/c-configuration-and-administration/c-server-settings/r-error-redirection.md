---
description: Use essas configurações do servidor para redirecionar erros.
solution: Experience Manager
title: Redirecionamento de erro
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Redirecionamento de erro{#error-redirection}

Use essas configurações do servidor para redirecionar erros.

>[!NOTE]
>
>Caracteres de barra vertical (|) no caminho de rede não são suportados para redirecionamento de erro.

## PS::errorRedirect.rootUrl - Servidor de redirecionamento {#section-85f22e48d68842a490b0e1191543b558}

A URL raiz ( HTTP:// *[!DNL domain]*[: *[!DNL port]*]) da implantação secundária do Servidor de Imagens para a qual as solicitações que falharem localmente devem ser redirecionadas. O redirecionamento de erro está desativado (padrão) quando essa configuração está vazia ou não está definida.

## PS::errorRedirect.connectTimeout - Tempo Limite de Conexão de Redirecionamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo máximo (em ms) que o servidor aguarda uma conexão com o servidor secundário ser estabelecida antes de retornar um erro ao cliente.

## PS::errorRedirect.socketTimeout - Tempo limite de resposta de redirecionamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo máximo (em ms) que o servidor aguarda o servidor secundário retornar dados antes de abandonar a solicitação de redirecionamento e retornar um erro ao cliente.
