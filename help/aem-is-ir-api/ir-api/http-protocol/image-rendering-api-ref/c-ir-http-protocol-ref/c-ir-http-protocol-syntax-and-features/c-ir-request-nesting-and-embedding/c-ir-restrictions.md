---
description: Algumas restrições se aplicam ao aninhamento e incorporação.
seo-description: Algumas restrições se aplicam ao aninhamento e incorporação.
seo-title: Restrições
solution: Experience Manager
title: Restrições
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura dos objetos aos quais o material está sendo aplicado.

As imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente depois que a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
