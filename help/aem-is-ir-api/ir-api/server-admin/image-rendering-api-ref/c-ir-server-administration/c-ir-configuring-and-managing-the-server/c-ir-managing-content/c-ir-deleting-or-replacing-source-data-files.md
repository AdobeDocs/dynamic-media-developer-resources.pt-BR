---
description: Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes de o arquivo ser substituído.
seo-description: Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes de o arquivo ser substituído.
seo-title: Exclusão ou substituição de arquivos de dados de origem
solution: Experience Manager
title: Exclusão ou substituição de arquivos de dados de origem
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Excluir ou substituir arquivos de dados de origem{#deleting-or-replacing-source-data-files}

Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes de o arquivo ser substituído.

>[!NOTE]
>
>Um arquivo de dados não deve ser substituído ou excluído enquanto o Servidor de Renderização estiver acessando.

Lembre-se de que excluir ou substituir um arquivo de dados de origem faz com que o Servidor de Renderização feche o arquivo até a próxima solicitação que acessar a vinheta. Várias tentativas podem ser necessárias se um arquivo for muito usado.

O Servidor de Renderização deve ser interrompido para substituir outros arquivos de dados.

As entradas de cache do Platform Server são automaticamente invalidadas quando os arquivos de material ou as vinhetas são substituídos. Substituir arquivos de perfil ICC não invalida os caches.

Para evitar as complicações da substituição de arquivos, é recomendável dar um novo nome a um arquivo de substituição e atualizar as entradas de catálogo correspondentes. Isso permite a substituição de qualquer arquivo de dados enquanto o servidor está ativo e faz com que as entradas de cache do servidor fiquem obsoletas automaticamente sem nenhuma intervenção adicional. Essa abordagem pode ser usada para todos os arquivos de dados gerenciados por catálogos de imagens.
