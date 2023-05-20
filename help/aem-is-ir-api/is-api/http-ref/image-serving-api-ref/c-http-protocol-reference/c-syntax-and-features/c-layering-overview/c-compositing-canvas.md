---
description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.

A Camada 0 constitui a camada de plano de fundo, que é sempre necessária e que define o tamanho da imagem composta. Qualquer tipo de camada é permitido para a camada 0. O tamanho da camada 0 deve ser definido, utilizando explicitamente `size=` ou implicitamente, com base na imagem do conteúdo ou texto. Quaisquer áreas de outras camadas que estejam fora da área da camada 0 não serão incluídas na imagem de saída.

>[!NOTE]
>
>Depois que todas as camadas forem niveladas, a imagem composta será convertida na imagem de resposta final, conforme especificado com [exibir comandos e atributos](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
