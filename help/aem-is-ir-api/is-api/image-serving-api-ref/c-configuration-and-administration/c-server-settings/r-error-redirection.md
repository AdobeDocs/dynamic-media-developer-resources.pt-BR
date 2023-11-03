---
description: Use essas configurações do servidor para redirecionar erros.
solution: Experience Manager
title: Redirecionamento de erro
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Redirecionamento de erro{#error-redirection}

Use essas configurações do servidor para redirecionar erros.

>[!NOTE]
>
>Caracteres de barra vertical (|) no caminho de rede não são suportados para redirecionamento de erro.

## PS::errorRedirect.rootUrl - Servidor de redirecionamento {#section-85f22e48d68842a490b0e1191543b558}

O URL raiz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]]) para a implantação do Servidor de imagens secundário para o qual as solicitações que falharem localmente deverão ser redirecionadas. O redirecionamento de erro está desativado (padrão) quando essa configuração está vazia ou não está definida.

## PS::errorRedirect.connectTimeout - Tempo Limite de Conexão de Redirecionamento {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo máximo (em ms) que o servidor aguarda uma conexão com o servidor secundário ser estabelecida antes de retornar um erro ao cliente.

## PS::errorRedirect.socketTimeout - Tempo limite de resposta de redirecionamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo máximo (em ms) que o servidor aguarda o servidor secundário retornar dados antes de abandonar a solicitação de redirecionamento e retornar um erro ao cliente.
