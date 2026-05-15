---
description: Este é o log primário que controla todas as solicitações HTTP feitas em  [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.
solution: Experience Manager
title: Log de acesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# Log de acesso{#access-log}

Este é o log primário que controla todas as solicitações HTTP feitas para o [!DNL Platform Server]. A Renderização de imagem, se ativada, grava seus dados de log de acesso no mesmo arquivo.

O log de acesso é configurado em server.xml.

>[!NOTE]
>
>Além do tráfego de cliente do Servidor de imagens ( [!DNL /is/image/*]) e da Renderização de imagens ( [!DNL /ir/render/*]), o log de acesso pode incluir determinado tráfego interno: acesso ao sistema de catálogo [!DNL Platform Server] ( [!DNL /is-catalog/*]), compartilhamento de cache e solicitações de redirecionamento de erro ( [!DNL /is/cache/*]), acesso a outros pacotes implantados no [!DNL Platform Server], como os Visualizadores do Dynamic Media ( [!DNL /is-viewers/*]), tráfego estático e solicitações de conteúdo estático atendidas pelo [!DNL Platform Server] (por exemplo, [!DNL /is-docs/*]).

As solicitações com caminhos raiz [!DNL /is-catalog] e [!DNL /is/cache] devem ser sempre excluídas de qualquer análise de tráfego de cliente.
