---
description: Após a instalação, será necessário configurar os serviços para serem executados na outra conta de usuário.
seo-description: Após a instalação, será necessário configurar os serviços para serem executados na outra conta de usuário.
seo-title: Instalar em uma conta de usuário diferente do administrador
solution: Experience Manager
title: Instalar em uma conta de usuário diferente do administrador
uuid: c5944515-c378-45c3-bc18-3261133ba009
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# Instalar em uma conta de usuário diferente de administrador{#installing-under-a-different-user-account-than-administrator}

Após a instalação, será necessário configurar os serviços para serem executados na outra conta de usuário.

1. Acesse as configurações da Política de segurança local do Windows clicando em **[!UICONTROL Start Menu]** > **[!UICONTROL Settings]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administration Tools]** > **[!UICONTROL Local Security Policy]**.
1. Selecione **[!UICONTROL Security Settings]** > **[!UICONTROL Local Policies]** > **[!UICONTROL User Rights Assignment]**.
1. Clique duas vezes na política &quot;Fazer logon como um serviço&quot;.
1. Clique em **[!UICONTROL Add…]**, selecione o Usuário ou Grupo e clique em **[!UICONTROL Ok]** para confirmar.
