---
description: Os arquivos de dados da fonte de conteúdo estático são acessados somente pelo Servidor de plataforma.
seo-description: Os arquivos de dados da fonte de conteúdo estático são acessados somente pelo Servidor de plataforma.
seo-title: Dados da fonte de conteúdo estático
solution: Experience Manager
title: Dados da fonte de conteúdo estático
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Dados da fonte de conteúdo estático{#static-content-source-data}

Os arquivos de dados da fonte de conteúdo estático são acessados somente pelo Servidor de plataforma.

O caminho para arquivos de dados de conteúdo estático é resolvido da seguinte maneira:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos os segmentos ` *[!DNL rootPath]*` podem ser segmentos de caminho vazios, relativos ou absolutos.

` *[!DNL catalogPath]*` é um caminho/nome de arquivo absoluto ou relativo. *[!DNL requestPath]* deve ser um caminho/nome de arquivo relativo.

Vários valores `PS::staticContent.rootPaths` podem ser definidos em [!DNL PlatformServer.conf]. Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor da Plataforma tentará caminhos alternativos na ordem especificada até que o arquivo de dados seja encontrado.
