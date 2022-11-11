---
description: Este é o log principal que mantém o controle de todas as solicitações HTTP feitas ao [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
solution: Experience Manager
title: Log de acesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Log de acesso{#access-log}

Este é o log principal que mantém o controle de todas as solicitações HTTP feitas ao [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.

O log de acesso é configurado em server.xml.

>[!NOTE]
>
>Além do tráfego do cliente para o Image Serving ( [!DNL /is/image/*]) e Renderização de imagem ( [!DNL /ir/render/*]), o log de acesso pode incluir determinado tráfego interno: acesso ao [!DNL Platform Server] sistema de catálogo ( [!DNL /is-catalog/*]), compartilhamento de cache e solicitações de redirecionamento de erro ( [!DNL /is/cache/*]), acesso a outros pacotes implantados no [!DNL Platform Server], como Visualizadores do Dynamic Media ( [!DNL /is-viewers/*]), tráfego estático e solicitações de conteúdo estático atendidas pelo [!DNL Platform Server] (por exemplo, [!DNL /is-docs/*]).

Solicitações com [!DNL /is-catalog] e [!DNL /is/cache] os caminhos raiz devem sempre ser excluídos de qualquer análise de tráfego de cliente.
