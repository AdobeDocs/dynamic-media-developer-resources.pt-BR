---
description: Defina a margem da mídia. Define a margem de mídia definida no arquivo PDF.
seo-description: Defina a margem da mídia. Define a margem de mídia definida no arquivo PDF.
seo-title: mediaMargin
solution: Experience Manager
title: mediaMargin
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e72f4791-d5c7-4b4d-90dd-39b478640abd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# mediaMargin{#mediamargin}

Defina a margem da mídia. Define a margem de mídia definida no arquivo PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, `mediaMargin` está definido para o tamanho completo do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* são padronizados para o valor *[!DNL top]* se não for especificado.
