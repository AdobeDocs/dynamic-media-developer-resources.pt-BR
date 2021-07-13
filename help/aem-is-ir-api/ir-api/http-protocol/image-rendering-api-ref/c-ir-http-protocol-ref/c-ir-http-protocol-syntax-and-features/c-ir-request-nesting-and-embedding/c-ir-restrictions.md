---
description: Algumas restrições se aplicam ao aninhamento e à incorporação.
solution: Experience Manager
title: Restrições
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e à incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura do(s) objeto(s) ao(s) qual(is) o material está sendo aplicado.

Imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente após a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
