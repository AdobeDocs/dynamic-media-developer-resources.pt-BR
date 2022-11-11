---
description: Os arquivos de dados da fonte de conteúdo estático são acessados somente pelo [!DNL Platform Server].
solution: Experience Manager
title: Dados da fonte de conteúdo estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Dados da fonte de conteúdo estático{#static-content-source-data}

Os arquivos de dados da fonte de conteúdo estático são acessados somente pelo [!DNL Platform Server].

O caminho para arquivos de dados de conteúdo estático é resolvido da seguinte maneira:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos ` *[!DNL rootPath]*` segmentos podem ser segmentos de caminho vazios, relativos ou absolutos.

` *[!DNL catalogPath]*` é um caminho/nome de arquivo absoluto ou relativo. *[!DNL requestPath]* deve ser um caminho/nome de arquivo relativo.

Vários `PS::staticContent.rootPaths` podem ser definidos em [!DNL PlatformServer.conf]. Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O [!DNL Platform Server] tentará caminhos alternativos na ordem especificada até que o arquivo de dados seja encontrado.
