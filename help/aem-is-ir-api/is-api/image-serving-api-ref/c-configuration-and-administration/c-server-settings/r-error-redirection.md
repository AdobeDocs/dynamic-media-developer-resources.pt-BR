---
description: Use essas configurações do servidor para redirecionar erros.
solution: Experience Manager
title: Redirecionamento de erro
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Redirecionamento de erro{#error-redirection}

Use essas configurações do servidor para redirecionar erros.

>[!NOTE]
>
>Caracteres de barra vertical (|) no caminho de rede não são suportados para redirecionamento de erro.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

O URL raiz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) para a implantação secundária do Image Serving, à qual as solicitações que falharem localmente devem ser redirecionadas. O redirecionamento de erro é desativado (padrão) quando essa configuração está vazia ou não está definida.

## PS::errorRedirect.connectTimeout - Tempo limite da conexão de redirecionamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo máximo (em ms) que o servidor aguardará para que uma conexão com o servidor secundário seja estabelecida antes de retornar um erro ao cliente.

## PS::errorRedirect.socketTimeout - Tempo limite de resposta de redirecionamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo máximo (em ms) que o servidor aguardará o servidor secundário retornar os dados antes de abandonar a solicitação de redirecionamento e retornar um erro ao cliente.
