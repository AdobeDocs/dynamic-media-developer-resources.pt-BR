---
description: A etapa 2 das transformações de camada de imagem é modificada da seguinte forma para miniaturas (ou seja, se req=tmb).
seo-description: A etapa 2 das transformações de camada de imagem é modificada da seguinte forma para miniaturas (ou seja, se req=tmb).
seo-title: Escala em miniatura
solution: Experience Manager
title: Escala em miniatura
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Dimensionamento em miniatura{#thumbnail-scaling}

A etapa 2 das transformações de camada de imagem é modificada da seguinte forma para miniaturas (ou seja, se req=tmb).

* `2.` Se  `size=` for especificado, ajuste a imagem (cortada) no  `size=` retângulo usando as regras de miniatura. Se `size=` não for especificado, ajuste a escala com base em `res=` ou, se `res=` não for especificado, ajuste a imagem (cortada) para o retângulo usando as regras de miniatura descritas abaixo.

