---
description: As configurações de renderização de imagem são armazenadas no arquivo de configuração do Servidor de plataforma.
solution: Experience Manager
title: Arquivos de configuração
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Arquivos de configuração{#configuration-files}

As configurações de renderização de imagem são armazenadas no arquivo de configuração do Servidor de plataforma.

O arquivo de configuração do servidor da plataforma está localizado em [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Esse arquivo é um arquivo de propriedades JAVA. Deve-se tomar cuidado para seguir as convenções apropriadas, caso contrário, o Servidor da plataforma pode não conseguir iniciar. Uma barra invertida dupla (`\\`) ou uma barra invertida única (/) deve ser usada em vez de uma barra invertida simples (\) nos caminhos de arquivo do Windows, porque a barra invertida é usada como um caractere de escape nesse tipo de arquivo. O arquivo contém propriedades não documentadas, que são para uso interno do servidor e não devem ser modificadas.

Consulte o [Referência de configurações](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obter uma lista de todas as configurações da Renderização de imagem.
