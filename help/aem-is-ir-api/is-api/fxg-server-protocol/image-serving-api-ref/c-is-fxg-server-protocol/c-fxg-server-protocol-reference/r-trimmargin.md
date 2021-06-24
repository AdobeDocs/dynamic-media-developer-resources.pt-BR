---
description: Defina a margem da aparação. Define a margem de corte que é definida no arquivo PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Defina a margem da aparação. Define a margem de corte que é definida no arquivo PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, `trimMargin` é definido no tamanho total do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* são padronizados para o valor *[!DNL top]* se não for especificado.
