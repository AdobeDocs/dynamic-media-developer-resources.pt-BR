---
description: Defina a margem da mídia. Define a margem de mídia que é definida no arquivo PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Defina a margem da mídia. Define a margem de mídia que é definida no arquivo PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, `mediaMargin` é definido no tamanho total do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* são padronizados para o valor *[!DNL top]* se não for especificado.
