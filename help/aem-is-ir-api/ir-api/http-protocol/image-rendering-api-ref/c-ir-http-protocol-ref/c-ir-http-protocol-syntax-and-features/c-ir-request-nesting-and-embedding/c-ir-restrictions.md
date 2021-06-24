---
description: Algumas restrições se aplicam ao aninhamento e à incorporação.
solution: Experience Manager
title: Restrições
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e à incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura do(s) objeto(s) ao(s) qual(is) o material está sendo aplicado.

Imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente após a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
