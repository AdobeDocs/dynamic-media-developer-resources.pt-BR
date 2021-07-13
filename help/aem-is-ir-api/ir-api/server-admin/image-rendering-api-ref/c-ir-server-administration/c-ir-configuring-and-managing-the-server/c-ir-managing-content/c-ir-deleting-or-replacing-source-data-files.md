---
description: Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes de o arquivo ser substituído.
solution: Experience Manager
title: Exclusão ou substituição de arquivos de dados de origem
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Exclusão ou substituição de arquivos de dados de origem{#deleting-or-replacing-source-data-files}

Os arquivos de vinheta podem ser substituídos ou excluídos enquanto o servidor está ativo usando o comando req=release logo antes de o arquivo ser substituído.

>[!NOTE]
>
>Um arquivo de dados não deve ser substituído ou excluído enquanto o Servidor de Renderização estiver acessando.

Lembre-se de que excluir ou substituir um arquivo de dados de origem faz com que o Servidor de Renderização feche o arquivo até a próxima solicitação que acessar a vinheta. Várias tentativas podem ser necessárias se um arquivo for muito usado.

O Servidor de Renderização deve ser interrompido para substituir outros arquivos de dados.

As entradas de cache do Platform Server são automaticamente invalidadas quando os arquivos de material ou as vinhetas são substituídos. Substituir arquivos de perfil ICC não invalida os caches.

Para evitar as complicações da substituição de arquivos, é recomendável dar um novo nome a um arquivo de substituição e atualizar as entradas de catálogo correspondentes. Isso permite a substituição de qualquer arquivo de dados enquanto o servidor está ativo e faz com que as entradas de cache do servidor fiquem obsoletas automaticamente sem nenhuma intervenção adicional. Essa abordagem pode ser usada para todos os arquivos de dados gerenciados por catálogos de imagens.
