---
description: Definir margem da mídia. Define a margem de mídia definida no arquivo PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Definir margem da mídia. Define a margem de mídia definida no arquivo PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, o `mediaMargin` está definido como o tamanho máximo do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* assumem como padrão o valor *[!DNL top]*, se não forem especificados.
