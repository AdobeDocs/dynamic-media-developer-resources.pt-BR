---
description: Use essas configurações de servidor para SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# SSL{#ssl}

Use essas configurações de servidor para SSL.

## TC::SslPort - Porta de escuta {#section-c80eb582bf684b3fa7313a77cc606769}

Especifica a porta de escuta para o Servidor da Plataforma para conexões SSL. O padrão é 8443.

## TC::keystoreFile - Caminho do Arquivo do Armazenamento de Chaves {#section-0cdf9b3cfcf249818b22221d01bafebe}

Especifique o caminho/nome do arquivo de repositório de chaves SSL. Pode ser um caminho absoluto ou um caminho relativo a [!DNL *[!DNL install_folder]*/conf]. O padrão é *install_folder*/conf/scene7keystore.

## TC::keystorePass - Senha do Armazenamento de Chaves {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

A senha do arquivo do repositório de chaves. O padrão é `scene7`.

## TC::keystoreType - Tipo de Armazenamento de Chaves {#section-8f263e1ba67740728cd39181960d7c7d}

Selecione o tipo de armazenamento de chaves. Há suporte para &#39; `Java'` (padrão) e &#39; `PKCS12`&#39;.
