---
description: Algumas restrições se aplicam ao aninhamento e à incorporação.
seo-description: Algumas restrições se aplicam ao aninhamento e à incorporação.
seo-title: Restrições
solution: Experience Manager
title: Restrições
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e à incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura do(s) objeto(s) ao(s) qual(is) o material está sendo aplicado.

Imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente após a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
