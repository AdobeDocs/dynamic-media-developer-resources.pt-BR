---
description: As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

As camadas são compostas na ordem especificada pelo comando layer=, onde as camadas com números mais altos ocultam as com números mais baixos.

A Camada 0 constitui a camada de plano de fundo, que é sempre necessária e que define o tamanho da imagem composta. Qualquer tipo de camada é permitido para a camada 0. O tamanho da camada 0 deve ser definido, usando explicitamente `size=` ou implicitamente, com base na imagem de conteúdo ou texto. Quaisquer áreas de outras camadas que estejam fora da área da camada 0 não são incluídas na imagem de saída.

>[!NOTE]
>
>Depois que todas as camadas forem niveladas, a imagem composta será convertida na imagem de resposta final, conforme especificado com os [comandos e atributos de exibição](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
