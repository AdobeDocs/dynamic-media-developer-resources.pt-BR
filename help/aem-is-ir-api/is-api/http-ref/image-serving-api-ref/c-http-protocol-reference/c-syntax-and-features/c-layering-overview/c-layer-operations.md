---
description: Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).
solution: Experience Manager
title: Operações de camada
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Operações de camada{#layer-operations}

Além de dimensionar (size=) e posicionar (pos=) camadas em relação à camada 0 e especificar a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).

Os atributos `origin=` e `anchor=` podem ser usados para manter o alinhamento desejado entre as camadas quando imagens ou texto são alterados dinamicamente em modelos.

O comando `maskUse=` está disponível para camadas de imagem para acessar a área de plano de fundo de imagens que têm máscaras separadas.

`opac=` pode ser usada para variar a opacidade da camada e  `hide=` para mostrar ou ocultar a camada.
