---
description: Use essas configurações de servidor para SSL.
seo-description: Use essas configurações de servidor para SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# SSL{#ssl}

Use essas configurações de servidor para SSL.

## TC::SslPort - Porta de escuta {#section-c80eb582bf684b3fa7313a77cc606769}

Especifica a porta de escuta para as conexões SSL do Servidor de Plataformas. O padrão é 8443.

## TC::keystoreFile - Caminho do Arquivo do Keystore {#section-0cdf9b3cfcf249818b22221d01bafebe}

Especifique o caminho/nome do arquivo de armazenamento de chaves SSL. Pode ser um caminho absoluto ou um caminho relativo a [!DNL *[!DNL install_folder]*/conf]. O padrão é *install_folder*/conf/cena7keystore.

## TC::keystorePass - Senha do Keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

A senha do arquivo de armazenamento de chaves. O padrão é `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Selecione o tipo de armazenamento de chaves. &#39; `Java'` (padrão) e &#39; `PKCS12`&#39; são suportados.
