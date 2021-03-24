---
description: Na sequência de comando do Modificador de URL ou catálogo, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando event= ou o final do URL.
solution: Experience Manager
title: Especificação de camadas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Especificação de camadas{#specifying-layers}

Na sequência de comando URL ou catalog::Modifier, uma sequência de definição de camada começa com o comando layer= e termina com outro comando layer=, um comando event= ou o final do URL.

Todos os comandos na sequência de definição de camada são associados à camada.

O comando `layer=` especifica um número de camada, que deve ser um número inteiro 0 ou maior. Todos os comandos nas sequências de definição de camada com o mesmo número de camada são aplicados à mesma camada. Se o mesmo comando ocorrer mais de uma vez, a última instância prevalecerá.
