---
description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.

A Camada 0 constitui a camada de plano de fundo, que é sempre necessária e que define o tamanho da imagem composta. Qualquer tipo de camada é permitido para a camada 0. O tamanho da camada 0 deve ser definido, usando explicitamente `size=` ou implicitamente, com base na imagem de conteúdo ou texto. Quaisquer áreas de outras camadas que estejam fora da área da camada 0 não são incluídas na imagem de saída.

>[!NOTE]
>
>Depois que todas as camadas forem niveladas, a imagem composta será convertida na imagem de resposta final, conforme especificado com os [comandos e atributos de exibição](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
