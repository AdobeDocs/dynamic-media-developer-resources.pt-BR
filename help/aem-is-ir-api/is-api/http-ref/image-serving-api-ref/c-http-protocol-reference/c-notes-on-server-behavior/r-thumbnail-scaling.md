---
description: A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).
seo-description: A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).
seo-title: Escala de miniaturas
solution: Experience Manager
title: Escala de miniaturas
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Escala de miniaturas{#thumbnail-scaling}

A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).

* `2.` Se  `size=` for especificado, ajuste a imagem (cortada) no  `size=` retângulo usando as regras de miniatura. Se `size=` não for especificado, ajuste a escala com base em `res=` ou, se `res=` não for especificado, ajuste a imagem (cortada) no retângulo da tela usando as regras de miniatura descritas abaixo.

