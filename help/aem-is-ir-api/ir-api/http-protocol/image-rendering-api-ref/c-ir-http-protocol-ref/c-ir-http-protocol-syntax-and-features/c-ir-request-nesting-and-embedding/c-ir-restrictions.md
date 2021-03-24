---
description: Algumas restrições se aplicam ao aninhamento e à incorporação.
solution: Experience Manager
title: Restrições
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Restrições{#restrictions}

Algumas restrições se aplicam ao aninhamento e à incorporação.

Para um bom desempenho do servidor, a resolução de imagens retornadas por solicitações aninhadas deve corresponder razoavelmente à resolução de textura do(s) objeto(s) ao(s) qual(is) o material está sendo aplicado.

Imagens estrangeiras são armazenadas em cache localmente. Quaisquer alterações nessas imagens serão detectadas somente após a entrada do cache local se tornar obsoleta (com base no cabeçalho HTTP expirado).
