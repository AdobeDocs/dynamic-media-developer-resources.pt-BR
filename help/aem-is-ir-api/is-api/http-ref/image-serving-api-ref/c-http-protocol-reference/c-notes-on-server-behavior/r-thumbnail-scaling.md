---
description: A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).
solution: Experience Manager
title: Escala de miniaturas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Escala de miniaturas{#thumbnail-scaling}

A etapa 2 das transformações da camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, if req=tmb).

* `2.` Se  `size=` for especificado, ajuste a imagem (cortada) no  `size=` retângulo usando as regras de miniatura. Se `size=` não for especificado, ajuste a escala com base em `res=` ou, se `res=` não for especificado, ajuste a imagem (cortada) no retângulo da tela usando as regras de miniatura descritas abaixo.

