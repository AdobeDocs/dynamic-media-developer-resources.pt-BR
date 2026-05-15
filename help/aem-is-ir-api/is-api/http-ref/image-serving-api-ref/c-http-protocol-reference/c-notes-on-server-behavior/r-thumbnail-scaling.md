---
title: Dimensionamento de miniatura
description: A etapa 2 das transformações de camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, se req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# Dimensionamento de miniatura{#thumbnail-scaling}

A etapa 2 das transformações de camada de imagem é modificada da seguinte maneira para miniaturas (ou seja, se req=tmb).

* `2.` Se `size=` for especificado, ajustar a imagem (cortada) no retângulo `size=` usando as regras de miniatura. Se `size=` não for especificado, dimensione com base em `res=` ou, se `res=` não for especificado, ajuste a imagem (cortada) na tela de desenho usando as regras de miniatura descritas abaixo.
