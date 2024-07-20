---
title: Utilização de múltiplos mapas de iluminação
description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Utilização de múltiplos mapas de iluminação{#using-multiple-illumination-maps}

Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.

Até três mapas de iluminação podem ser criados para cada vinheta. O mapa de iluminação para uma operação de renderização é selecionado com os comandos `illum=` e/ou `gloss=`.

**Seleção padrão** - Se `illum=` ou `gloss=` não forem especificados, o renderizador usará o primeiro mapa de iluminação criado (normalmente, o mapa A, também conhecido como o mapa de iluminação &quot;Plano&quot;).

**Seleção automática com`gloss=`** - Se `illum=` não estiver especificado ou estiver definido como `-1`, o renderizador compara o valor `gloss=` especificado com os valores de brilho associados a cada mapa de iluminação na vinheta. Ele escolhe o mapa de iluminação cujo valor de brilho está mais próximo do `gloss=` especificado.

**Seleção explícita com`illum=`** - Se `illum=` for especificado e definido como `0`, `1` ou `2`, o renderizador usará o mapa de iluminação correspondente; `gloss=` será ignorado para selecionar o mapa de iluminação.

Se a vinheta contiver apenas um mapa de iluminação, o renderizador usará esse mapa e ignorará os comandos `illum=` e `gloss=`.
