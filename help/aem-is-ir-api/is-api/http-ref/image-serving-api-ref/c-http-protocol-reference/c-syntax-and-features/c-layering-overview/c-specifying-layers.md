---
description: Na sequência de comando do modificador de URL ou catálogo, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando effect= ou o fim do URL.
solution: Experience Manager
title: Especificação de camadas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Especificação de camadas{#specifying-layers}

Na sequência de comando URL or catalog::Modifier, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando effect= ou o fim do URL.

Todos os comandos na sequência de definição da camada são associados à camada.

A variável `layer=` especifica um número de camada, que deve ser um inteiro 0 ou maior. Todos os comandos em sequências de definição de camada com o mesmo número de camada são aplicados à mesma camada. Se o mesmo comando ocorrer mais de uma vez, a última instância prevalecerá.
