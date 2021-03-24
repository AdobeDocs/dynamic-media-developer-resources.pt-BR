---
description: Use essas configurações do servidor para redirecionar erros.
solution: Experience Manager
title: Redirecionamento de erro
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Redirecionamento de erro{#error-redirection}

Use essas configurações do servidor para redirecionar erros.

>[!NOTE]
>
>Caracteres de barra vertical (|) no caminho de rede não são suportados para redirecionamento de erro.

## PS::errorRedirect.rootUrl - Redirect Server {#section-85f22e48d68842a490b0e1191543b558}

O URL raiz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) para a implantação secundária do Image Serving, à qual as solicitações que falharem localmente devem ser redirecionadas. O redirecionamento de erro é desativado (padrão) quando essa configuração está vazia ou não está definida.

## PS::errorRedirect.connectTimeout - Tempo Limite da Conexão de Redirecionamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo máximo (em ms) que o servidor aguardará para que uma conexão com o servidor secundário seja estabelecida antes de retornar um erro ao cliente.

## PS::errorRedirect.socketTimeout - Tempo Limite de Resposta de Redirecionamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo máximo (em ms) que o servidor aguardará o servidor secundário retornar os dados antes de abandonar a solicitação de redirecionamento e retornar um erro ao cliente.
