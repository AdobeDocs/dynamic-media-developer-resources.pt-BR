---
description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com numeração mais alta ocultam as com numeração mais baixa.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com numeração mais alta ocultam as com numeração mais baixa.

A camada 0 constitui a camada de plano de fundo, que é sempre necessária e que define o tamanho da imagem composta. Qualquer um dos tipos de camada é permitido para a camada 0. O tamanho da camada 0 deve ser definido, usando explicitamente `size=` ou implicitamente, com base na imagem de conteúdo ou no texto. Quaisquer áreas de outras camadas que não se enquadrem na área da camada 0 não serão incluídas na imagem de saída.

>[!NOTE]
>
>Depois que todas as camadas são niveladas, a imagem composta é convertida na imagem de resposta final, conforme especificado com os [comandos e atributos de exibição](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
