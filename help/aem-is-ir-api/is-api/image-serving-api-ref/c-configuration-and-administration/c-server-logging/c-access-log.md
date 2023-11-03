---
description: Esse é o log primário que rastreia todas as solicitações HTTP feitas no [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
solution: Experience Manager
title: Log de acesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Log de acesso{#access-log}

Esse é o log primário que rastreia todas as solicitações HTTP feitas no [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.

O log de acesso é configurado em server.xml.

>[!NOTE]
>
>Além do tráfego de cliente para o Servidor de imagens ( [!DNL /is/image/*]) e Renderização de imagem ( [!DNL /ir/render/*]), o registro de acesso pode incluir determinado tráfego interno: acesso à [!DNL Platform Server] sistema de catálogo ( [!DNL /is-catalog/*]), compartilhamento de cache e solicitações de redirecionamento de erro ( [!DNL /is/cache/*]), acesso a outros pacotes implantados no [!DNL Platform Server], como os Visualizadores do Dynamic Media ( [!DNL /is-viewers/*]), tráfego estático e solicitações de conteúdo estático atendidas pelo [!DNL Platform Server] (por exemplo, [!DNL /is-docs/*]).

Solicitações com [!DNL /is-catalog] e [!DNL /is/cache] os caminhos raiz devem sempre ser excluídos de qualquer análise de tráfego do cliente.
