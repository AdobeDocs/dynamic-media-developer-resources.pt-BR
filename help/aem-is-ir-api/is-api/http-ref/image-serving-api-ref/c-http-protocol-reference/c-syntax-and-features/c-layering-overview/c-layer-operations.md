---
description: Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).
solution: Experience Manager
title: Operações de camada
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Operações de camada{#layer-operations}

Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).

Os atributos `origin=` e `anchor=` podem ser usados para manter o alinhamento desejado entre as camadas quando imagens ou texto são alterados dinamicamente em modelos.

O comando `maskUse=` está disponível para camadas de imagem para acessar a área de plano de fundo de imagens que têm máscaras separadas.

`opac=` pode ser usada para variar a opacidade da camada e  `hide=` para mostrar ou ocultar a camada.
