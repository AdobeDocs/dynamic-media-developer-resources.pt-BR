---
description: Algumas restrições se aplicam ao aninhamento e à incorporação.
solution: Experience Manager
title: Restrições
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e à incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura do(s) objeto(s) ao(s) qual(is) o material está sendo aplicado.

Imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente após a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
