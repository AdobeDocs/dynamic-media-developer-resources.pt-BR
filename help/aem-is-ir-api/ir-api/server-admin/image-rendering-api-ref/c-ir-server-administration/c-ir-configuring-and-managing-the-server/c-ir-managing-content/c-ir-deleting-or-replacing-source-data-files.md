---
description: Os arquivos de Vinheta podem ser substituídos ou excluídos enquanto o servidor estiver ativo, usando o comando req=release pouco antes de o arquivo ser substituído.
solution: Experience Manager
title: Exclusão ou substituição de arquivos de dados de origem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# Exclusão ou substituição de arquivos de dados de origem{#deleting-or-replacing-source-data-files}

Os arquivos de Vinheta podem ser substituídos ou excluídos enquanto o servidor estiver ativo, usando o comando req=release pouco antes de o arquivo ser substituído.

>[!NOTE]
>
>Um arquivo de dados não deve ser substituído ou excluído enquanto o Servidor de renderização estiver acessando-o.

Lembre-se de que excluir ou substituir um arquivo de dados de origem faz com que o Servidor de renderização feche o arquivo até a próxima solicitação que acessar essa vinheta. Várias tentativas podem ser necessárias se um arquivo for muito usado.

O Servidor de Renderização deve ser interrompido para substituir outros arquivos de dados.

[!DNL Platform Server] entradas de cache são invalidadas automaticamente quando arquivos de material ou vinhetas são substituídos. Substituir os arquivos de perfil ICC não invalida os caches.

Para evitar as complicações da substituição de arquivos, é recomendável dar um novo nome a um arquivo de substituição e atualizar as entradas de catálogo correspondentes. Isso permite a substituição de qualquer arquivo de dados enquanto o servidor estiver ativo e faz com que as entradas de cache do servidor se tornem obsoletas automaticamente sem intervenção adicional. Essa abordagem pode ser usada para todos os arquivos de dados gerenciados por catálogos de imagens.

