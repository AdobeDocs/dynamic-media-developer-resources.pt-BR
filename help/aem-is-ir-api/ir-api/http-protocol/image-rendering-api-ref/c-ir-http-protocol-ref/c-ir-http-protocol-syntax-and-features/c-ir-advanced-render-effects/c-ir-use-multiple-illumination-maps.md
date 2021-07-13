---
description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
solution: Experience Manager
title: Uso de mapas de iluminação múltipla
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Uso de mapas de iluminação múltipla{#using-multiple-illumination-maps}

Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.

Até três mapas de iluminação podem ser criados para cada vinheta. O mapa de iluminação para uma operação de renderização é selecionado com os comandos `illum=` e ou `gloss=`.

**** Seleção padrãoSe não  `illum=` nem  `gloss=` forem especificadas, o renderizador usará o primeiro mapa de iluminação criado (normalmente, mapa A, também conhecido como mapa de iluminação &quot;Simples&quot;).

**Seleção automática com`gloss=`** Se não  `illum=` for especificado ou se estiver definido como -1, o renderizador compara o  `gloss=` valor especificado com os valores de brilho associados a cada mapa de iluminação na vinheta e escolhe o mapa de iluminação cujo valor de brilho é mais próximo do  `gloss=`especificado.

**Seleção explícita com`illum=`** Se  `illum=` for especificado e definido como 0, 1 ou 2, o renderizador utilizará o mapa de iluminação correspondente;  `gloss=` é ignorada para efeitos de seleção do mapa de iluminação.

Se a vinheta contiver apenas um mapa de iluminação, o renderizador usará esse mapa e ignorará os comandos `illum=` e `gloss=`.
