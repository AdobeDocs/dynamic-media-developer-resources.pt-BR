---
description: Após a instalação, será necessário configurar os serviços para serem executados na outra conta de usuário.
solution: Experience Manager
title: Instalar em uma conta de usuário diferente do administrador
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 20bb00cb-3af6-4573-bbff-8c4f984ed2ae
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Instalar em uma conta de usuário diferente do administrador{#installing-under-a-different-user-account-than-administrator}

Após a instalação, será necessário configurar os serviços para serem executados na outra conta de usuário.

1. Acesse as configurações da Política de segurança local do Windows clicando em **[!UICONTROL Start Menu]** > **[!UICONTROL Settings]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administration Tools]** > **[!UICONTROL Local Security Policy]**.
1. Selecione **[!UICONTROL Security Settings]** > **[!UICONTROL Local Policies]** > **[!UICONTROL User Rights Assignment]**.
1. Clique duas vezes na política &quot;Fazer logon como um serviço&quot;.
1. Clique em **[!UICONTROL Add…]**, selecione o Usuário ou Grupo e clique em **[!UICONTROL Ok]** para confirmar.
