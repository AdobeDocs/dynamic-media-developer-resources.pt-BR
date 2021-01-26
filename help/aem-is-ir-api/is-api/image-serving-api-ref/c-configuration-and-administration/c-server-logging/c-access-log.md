---
description: Este é o registro principal que controla todas as solicitações HTTP feitas no Servidor de plataforma. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
seo-description: Este é o registro principal que controla todas as solicitações HTTP feitas no Servidor de plataforma. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
seo-title: Log de acesso
solution: Experience Manager
title: Log de acesso
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Log de acesso{#access-log}

Este é o registro principal que controla todas as solicitações HTTP feitas no Servidor de plataforma. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.

O log de acesso está configurado em server.xml.

>[!NOTE]
>
>Além do tráfego do cliente para o Serviço de imagem ( [!DNL /is/image/*]) e Renderização de imagem ( [!DNL /ir/render/*]), o log de acesso pode incluir determinados tráfegos internos: acesso ao sistema de catálogo do Servidor de Plataformas ( [!DNL /is-catalog/*]), compartilhamento de cache e solicitações de redirecionamento de erros ( [!DNL /is/cache/*]), acesso a outros pacotes implantados no Servidor de Plataformas, como os Visualizadores do Dynamic Media ( [!DNL /is-viewers/*]), tráfego estático e solicitações de conteúdo estático atendidas pelo Servidor de Plataformas (por exemplo, [!DNL /is-docs/*]).

As solicitações com os caminhos raiz [!DNL /is-catalog] e [!DNL /is/cache] devem ser sempre excluídas de qualquer análise de tráfego do cliente.
