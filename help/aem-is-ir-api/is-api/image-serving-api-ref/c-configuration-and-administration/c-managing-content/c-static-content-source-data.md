---
description: Os arquivos de dados de fonte de conteúdo estático são acessados somente pelo  [!DNL Platform Server].
solution: Experience Manager
title: Dados de fonte de conteúdo estático
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
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
