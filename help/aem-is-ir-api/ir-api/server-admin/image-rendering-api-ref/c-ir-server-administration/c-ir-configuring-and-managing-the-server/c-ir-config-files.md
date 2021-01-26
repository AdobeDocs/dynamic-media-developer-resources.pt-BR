---
description: As configurações de renderização de imagem são armazenadas no arquivo de configuração do Servidor de plataforma.
seo-description: As configurações de renderização de imagem são armazenadas no arquivo de configuração do Servidor de plataforma.
seo-title: Arquivos de configuração
solution: Experience Manager
title: Arquivos de configuração
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Arquivos de configuração{#configuration-files}

As configurações de renderização de imagem são armazenadas no arquivo de configuração do Servidor de plataforma.

O arquivo de configuração do servidor de plataforma está localizado em [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este arquivo é um arquivo de propriedades JAVA. É necessário ter cuidado para seguir as convenções apropriadas; caso contrário, o Servidor da plataforma poderá falhar no start. Uma barra invertida de duplo (`\\`) ou uma barra (/) deve ser usada em vez de uma barra invertida simples (\) nos caminhos de arquivos do Windows, pois a barra invertida é usada como um caractere de escape nesse tipo de arquivo. O arquivo contém propriedades não documentadas, que são para uso interno do servidor e não devem ser modificadas.

Consulte a [Referência de configurações](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obter uma lista de todas as configurações de renderização de imagem.
