---
description: Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e invertidas (flip=).
solution: Experience Manager
title: Operações de camada
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Operações de camada{#layer-operations}

Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e invertidas (flip=).

Os atributos `origin=` e `anchor=` podem ser usados para manter o alinhamento desejado entre camadas quando imagens ou texto são alterados dinamicamente em modelos.

O comando `maskUse=` está disponível para camadas de imagem acessarem a área de plano de fundo de imagens que têm máscaras separadas.

`opac=` pode ser usado para variar a opacidade da camada e `hide=` para mostrar ou ocultar a camada.
