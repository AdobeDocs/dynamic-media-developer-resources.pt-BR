---
description: A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).
solution: Experience Manager
title: Escala de miniaturas
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Escala de miniaturas{#thumbnail-scaling}

A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).

* `2.` Se  `size=` for especificado, ajuste a imagem (cortada) no  `size=` retângulo usando as regras de miniatura. Se `size=` não for especificado, ajuste a escala com base em `res=` ou, se `res=` não for especificado, ajuste a imagem (cortada) no retângulo da tela usando as regras de miniatura descritas abaixo.
