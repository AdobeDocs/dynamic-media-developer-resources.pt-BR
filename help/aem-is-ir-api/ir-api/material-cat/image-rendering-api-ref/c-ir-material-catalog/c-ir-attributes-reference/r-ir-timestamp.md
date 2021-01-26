---
description: Carimbo de data e hora de modificação padrão. Fornece um valor padrão para o catálogo TimeStamp e vinheta TimeStamp. Se não for especificado, o servidor usará a data/hora de modificação deste arquivo Catalog.ini.
seo-description: Carimbo de data e hora de modificação padrão. Fornece um valor padrão para o catálogo TimeStamp e vinheta TimeStamp. Se não for especificado, o servidor usará a data/hora de modificação deste arquivo Catalog.ini.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Carimbo de data e hora{#timestamp}

Carimbo de data e hora de modificação padrão. Fornece um valor padrão para catálogo::TimeStamp e vinheta::TimeStamp. Se não for especificado, o servidor usará a data/hora de modificação deste arquivo Catalog.ini.

## Propriedades {#section-910e2562b41c47b78ee6216deeabbbd5}

Valor de data/hora no formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* está no intervalo de 0 a 23.

*[!DNL zzz]* é um código de fuso horário de 3 ou 4 caracteres, como &#39;GMT&#39; ou &#39;PST&#39;. O Horário de Verão deve ser contabilizado no código do fuso horário (por exemplo, &#39;PST&#39; para o Horário Padrão do Pacífico, em vez de &#39;PDT&#39; para o Horário de Verão do Pacífico).

*[!DNL offset]* é um deslocamento de fuso horário em horas ou horas:minutos, em relação ao GMT. Por exemplo, &#39;PDT&#39; é equivalente a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados da string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *[!DNL catalog]*.ini] será usada.

## Padrão {#section-65fb29a9ea2044df8cb9fe295eb14872}

Se estiver vazio ou não estiver definido, o servidor usará a hora de modificação do arquivo deste arquivo [!DNL *[!DNL catalog]*.ini].

## Consulte também {#section-764188f9b1734ad1a6270f5fecd28532}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vinheta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
