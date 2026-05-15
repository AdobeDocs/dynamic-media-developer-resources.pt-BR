---
description: Na sequência de comando do modificador de URL ou catálogo, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando effect= ou o fim do URL.
solution: Experience Manager
title: Especificação de camadas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# Especificação de camadas{#specifying-layers}

Na sequência de comando URL or catalog::Modifier, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando effect= ou o fim do URL.

Todos os comandos na sequência de definição da camada são associados à camada.

O comando `layer=` especifica um número de camada, que deve ser um inteiro 0 ou maior. Todos os comandos em sequências de definição de camada com o mesmo número de camada são aplicados à mesma camada. Se o mesmo comando ocorrer mais de uma vez, a última instância prevalecerá.
