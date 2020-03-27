---
description: Na sequência de comandos URL ou Modificador de catálogo, uma sequência de definição de camada é start com o comando layer= e termina com outro comando layer=, um comando effect= ou o final do URL.
seo-description: Na sequência de comandos URL ou Modificador de catálogo, uma sequência de definição de camada é start com o comando layer= e termina com outro comando layer=, um comando effect= ou o final do URL.
seo-title: Especificação de camadas
solution: Experience Manager
title: Especificação de camadas
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Especificação de camadas{#specifying-layers}

Na sequência de comando URL ou catálogo::Modificador, uma sequência de definição de camada start com o comando layer= e termina com outro comando layer=, um comando effect= ou o final do URL.

Todos os comandos na sequência de definição de camada estão associados à camada.

O `layer=` comando especifica um número de camada, que deve ser um número inteiro 0 ou maior. Todos os comandos em sequências de definição de camada com o mesmo número de camada são aplicados à mesma camada. Se o mesmo comando ocorrer mais de uma vez, a última instância prevalecerá.
