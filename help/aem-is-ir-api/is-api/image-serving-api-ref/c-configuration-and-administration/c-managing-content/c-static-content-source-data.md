---
description: Os arquivos de dados de fonte de conteúdo estático são acessados somente pelo  [!DNL Platform Server].
solution: Experience Manager
title: Dados de fonte de conteúdo estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Dados de fonte de conteúdo estático{#static-content-source-data}

Os arquivos de dados de fonte de conteúdo estático são acessados somente pelo [!DNL Platform Server].

O caminho para arquivos de dados de conteúdo estático é resolvido da seguinte maneira:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos os ` *[!DNL rootPath]*` segmentos podem ser vazios, relativos ou absolutos.

` *[!DNL catalogPath]*` é um caminho/nome de arquivo absoluto ou relativo. *[!DNL requestPath]* deve ser um caminho/nome de arquivo relativo.

Vários valores `PS::staticContent.rootPaths` podem ser definidos em [!DNL PlatformServer.conf]. Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O [!DNL Platform Server] tenta caminhos alternativos na ordem especificada, até que o arquivo de dados seja encontrado.
