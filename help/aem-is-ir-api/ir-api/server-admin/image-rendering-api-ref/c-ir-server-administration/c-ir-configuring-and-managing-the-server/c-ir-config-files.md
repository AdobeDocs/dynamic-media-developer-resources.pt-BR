---
description: As definições de configuração de Renderização de Imagem são armazenadas no arquivo de configuração  [!DNL Platform Server] .
solution: Experience Manager
title: Arquivos de configuração
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Arquivos de configuração{#configuration-files}

As definições de configuração de Renderização de Imagem são armazenadas no arquivo de configuração [!DNL Platform Server].

O arquivo de configuração do Platform Server está localizado em [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este arquivo é um arquivo de propriedades JAVA. Tenha cuidado ao seguir as convenções apropriadas; caso contrário, [!DNL Platform Server] pode falhar ao iniciar. Uma barra invertida dupla (`\\`) ou uma única barra invertida (/) deve ser usada em vez de uma barra invertida simples (\) nos caminhos de arquivo do Windows, porque a barra invertida é usada como um caractere de escape neste tipo de arquivo. O arquivo contém propriedades não documentadas, que são para uso interno do servidor e não devem ser modificadas.

Consulte a [Referência das Configurações](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obter uma lista de todas as configurações de Renderização de Imagem.
