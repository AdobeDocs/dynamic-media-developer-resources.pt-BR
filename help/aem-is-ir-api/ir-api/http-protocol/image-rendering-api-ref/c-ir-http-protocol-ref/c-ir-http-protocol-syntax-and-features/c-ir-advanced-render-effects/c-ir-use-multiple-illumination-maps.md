---
description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
seo-description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
seo-title: Uso de mapas de iluminação múltipla
solution: Experience Manager
title: Uso de mapas de iluminação múltipla
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Uso de mapas de iluminação múltipla{#using-multiple-illumination-maps}

Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.

Até três mapas de iluminação podem ser criados para cada vinheta. O mapa de iluminação para uma operação de renderização é selecionado com os comandos `illum=` e ou `gloss=`.

**** Seleção padrãoSe não  `illum=` nem  `gloss=` forem especificadas, o renderizador usará o primeiro mapa de iluminação criado (normalmente, mapa A, também conhecido como mapa de iluminação &quot;Simples&quot;).

**Seleção automática com`gloss=`** Se não  `illum=` for especificado ou se estiver definido como -1, o renderizador compara o  `gloss=` valor especificado com os valores de brilho associados a cada mapa de iluminação na vinheta e escolhe o mapa de iluminação cujo valor de brilho é mais próximo do  `gloss=`especificado.

**Seleção explícita com`illum=`** Se  `illum=` for especificado e definido como 0, 1 ou 2, o renderizador utilizará o mapa de iluminação correspondente;  `gloss=` é ignorada para efeitos de seleção do mapa de iluminação.

Se a vinheta contiver apenas um mapa de iluminação, o renderizador usará esse mapa e ignorará os comandos `illum=` e `gloss=`.
