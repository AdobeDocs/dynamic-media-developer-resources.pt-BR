---
description: Use essas configurações do servidor para redirecionar erros.
seo-description: Use essas configurações do servidor para redirecionar erros.
seo-title: Redirecionamento de erro
solution: Experience Manager
title: Redirecionamento de erro
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Redirecionamento de erro{#error-redirection}

Use essas configurações do servidor para redirecionar erros.

>[!NOTE]
>
>Caracteres de Pipe (|) no caminho de rede não são suportados para redirecionamento de erro.

## PS::errorRedirect.rootUrl - Servidor de redirecionamento {#section-85f22e48d68842a490b0e1191543b558}

O URL raiz ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]) para a implantação secundária do Serviço de imagem para a qual as solicitações que falharem localmente devem ser redirecionadas. O redirecionamento de erro é desativado (padrão) quando essa configuração está vazia ou não está definida.

## PS::errorRedirect.connectTimeout - Tempo limite de redirecionamento da conexão {#section-3971be8f720d4b32a2cc7860b4085971}

Tempo máximo (em ms) que o servidor aguardará para que uma conexão com o servidor secundário seja estabelecida antes de retornar um erro ao cliente.

## PS::errorRedirect.socketTimeout - Tempo limite de resposta de redirecionamento {#section-69d8579f748d4044bca99dfb64dd523c}

Tempo máximo (em ms) que o servidor aguardará o servidor secundário retornar os dados antes de abandonar a solicitação de redirecionamento e retornar um erro ao cliente.
