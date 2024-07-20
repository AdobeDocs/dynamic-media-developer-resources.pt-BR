---
description: Definir margem de sangria. Define a margem de sangria definida no arquivo PDF.
solution: Experience Manager
title: margem de sangramento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# margem de sangramento{#bleedmargin}

Definir margem de sangria. Define a margem de sangria definida no arquivo PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, o `bleedMargin` está definido como o tamanho máximo do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* assumem como padrão o valor *[!DNL top]*, se não forem especificados.
