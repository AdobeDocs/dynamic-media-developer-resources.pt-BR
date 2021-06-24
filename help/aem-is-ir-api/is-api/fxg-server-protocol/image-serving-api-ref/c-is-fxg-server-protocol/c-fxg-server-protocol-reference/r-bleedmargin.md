---
description: Defina a margem de sangria. Define a margem de sangria definida no arquivo PDF.
solution: Experience Manager
title: margem
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# margem{#bleedmargin}

Defina a margem de sangria. Define a margem de sangria definida no arquivo PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, `bleedMargin` é definido no tamanho total do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* são padronizados para o valor *[!DNL top]* se não for especificado.
