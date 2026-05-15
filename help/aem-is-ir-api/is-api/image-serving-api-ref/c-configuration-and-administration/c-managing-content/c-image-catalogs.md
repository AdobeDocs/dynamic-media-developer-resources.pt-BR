---
description: Os catálogos de imagens fornecem muitas definições de configuração do servidor, assim como fontes, perfis ICC e macros de comandos.
solution: Experience Manager
title: Catálogos de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Catálogos de imagens{#image-catalogs}

Os catálogos de imagens fornecem muitas definições de configuração do servidor, assim como fontes, perfis ICC e macros de comandos.

Eles mapeiam ids de imagem e conteúdo estático usadas em solicitações para caminhos de arquivos reais, armazenam vários metadados de imagem, como mapas de imagem, e fornecem containers para modelos e conjuntos de imagens.

Os catálogos de imagens são acessados somente pelo [!DNL Platform Server], nunca pelo Servidor de imagens. Os arquivos de atributo de catálogo devem ter um sufixo .ini e ser colocados na pasta de catálogo de [!DNL Platform Server] ( `PS::CatalogFolder`). Pelo menos o catálogo de imagens padrão é necessário e deve ser preenchido com todos os atributos para o funcionamento correto do [!DNL Platform Server].
