---
title: Dimensionamento de miniatura
description: A etapa 2 das transformações de camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, se req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Dimensionamento de miniatura{#thumbnail-scaling}

A etapa 2 das transformações de camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, se req=tmb).

* `2.` Se `size=` for especificada, ajuste a imagem (cortada) na `size=` corrigir usando regras de miniatura. Se `size=` não é especificado, dimensionar com base em `res=`, ou, se `res=` não for especificada, ajuste a imagem (cortada) na tela de desenho usando as regras de miniatura descritas abaixo.
