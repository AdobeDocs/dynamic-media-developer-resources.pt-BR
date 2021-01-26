---
description: Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes que o arquivo seja substituído.
seo-description: Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes que o arquivo seja substituído.
seo-title: Exclusão ou substituição de arquivos de dados de origem
solution: Experience Manager
title: Exclusão ou substituição de arquivos de dados de origem
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Exclusão ou substituição de arquivos de dados de origem{#deleting-or-replacing-source-data-files}

Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes que o arquivo seja substituído.

>[!NOTE]
>
>Um arquivo de dados não deve ser substituído ou excluído enquanto o Servidor de renderização estiver acessando-o.

Lembre-se de que a exclusão ou substituição de um arquivo de dados de origem faz com que o Servidor de renderização feche o arquivo até a próxima solicitação que acessar a vinheta. Várias tentativas podem ser necessárias se um arquivo for muito usado.

O Servidor de Renderização deve ser interrompido para substituir outros arquivos de dados.

As entradas de cache do Servidor de plataforma são automaticamente invalidadas quando os arquivos de material ou as vinhetas são substituídos. A substituição de arquivos de perfil ICC não invalida caches.

Para evitar as complicações da substituição de arquivos, é recomendável dar um novo nome a um arquivo de substituição e atualizar as entradas de catálogo correspondentes. Isso permite a substituição de qualquer arquivo de dados enquanto o servidor estiver ativo e faz com que as entradas de cache do servidor fiquem obsoletas automaticamente sem nenhuma intervenção adicional. Essa abordagem pode ser usada para todos os arquivos de dados gerenciados por catálogos de imagens.
