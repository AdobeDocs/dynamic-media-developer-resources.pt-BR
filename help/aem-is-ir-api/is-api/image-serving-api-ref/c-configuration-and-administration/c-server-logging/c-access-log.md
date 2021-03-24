---
description: Este é o log principal que acompanha todas as solicitações HTTP feitas no Servidor de Plataforma. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
solution: Experience Manager
title: Log de acesso
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Log de acesso{#access-log}

Este é o log principal que acompanha todas as solicitações HTTP feitas no Servidor de Plataforma. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.

O log de acesso é configurado em server.xml.

>[!NOTE]
>
>Além do tráfego do cliente para o Serviço de imagem ( [!DNL /is/image/*]) e Renderização de imagem ( [!DNL /ir/render/*]), o log de acesso pode incluir determinado tráfego interno: acesso ao sistema de catálogo do Platform Server ( [!DNL /is-catalog/*]), compartilhamento de cache e solicitações de redirecionamento de erros ( [!DNL /is/cache/*]), acesso a outros pacotes implantados no Servidor de plataforma, como os Visualizadores do Dynamic Media ( [!DNL /is-viewers/*]), tráfego estático e solicitações de conteúdo estático atendidas pelo Servidor de plataforma (por exemplo, [!DNL /is-docs/*]).

As solicitações com [!DNL /is-catalog] e [!DNL /is/cache] caminhos raiz devem sempre ser excluídas de qualquer análise de tráfego de cliente.
