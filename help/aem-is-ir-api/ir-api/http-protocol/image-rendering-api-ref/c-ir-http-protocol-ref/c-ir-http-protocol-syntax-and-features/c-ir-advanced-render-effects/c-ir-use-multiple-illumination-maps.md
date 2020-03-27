---
description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
seo-description: Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.
seo-title: Uso de mapas de iluminação múltiplos
solution: Experience Manager
title: Uso de mapas de iluminação múltiplos
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Uso de mapas de iluminação múltiplos{#using-multiple-illumination-maps}

Algumas aplicações podem exigir um mapa de iluminação diferente para diferentes tipos de materiais.

Até três mapas de iluminação podem ser criados para cada vinheta. O mapa de iluminação para uma operação de renderização é selecionado com os comandos `illum=` e ou `gloss=` .

**Seleção** padrão Se não for especificado `illum=` nem `gloss=` for especificado, o renderizador usará o primeiro mapa de iluminação criado (normalmente mapa A, conhecido como mapa de iluminação &quot;plano&quot;).

**Seleção automática com`gloss=`**Se não`illum=`for especificada ou estiver definida como -1, o renderizador compara o`gloss=`valor especificado com os valores de brilho associados a cada mapa de iluminação na vinheta e escolha o mapa de iluminação cujo valor de brilho é mais próximo do especificado`gloss=`.

**Seleção explícita com`illum=`**Se`illum=`for especificado e definido como 0, 1 ou 2, o renderizador usará o mapa de iluminação correspondente; é`gloss=`ignorada para efeitos de seleção do mapa de iluminação.

Se a vinheta contiver apenas um mapa de iluminação, o renderizador usará esse mapa e ignorará os comandos `illum=` e `gloss=` .
