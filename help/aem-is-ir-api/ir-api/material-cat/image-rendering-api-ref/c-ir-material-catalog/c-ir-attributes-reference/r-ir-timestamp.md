---
title: Carimbo de data/hora
description: Carimbo de data/hora de modificação padrão. Fornece um valor padrão para TimeStamp do catálogo e TimeStamp da vinheta. Se não for especificado, o servidor usará a data/hora de modificação desse arquivo catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
TQID: 'https://experienceleague.adobe.com/p3g5NQf25sagtaAYjdd4Vd8J6kZBAoLM8tSY42NPuOI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 6%

---

# Carimbo de data/hora{#timestamp}

Carimbo de data/hora de modificação padrão. Fornece um valor padrão para `catalog::TimeStamp` e `vignette::TimeStamp`. Se não for especificado, o servidor usará a data/hora de modificação desse arquivo catalog.ini.

## Propriedades {#section-910e2562b41c47b78ee6216deeabbbd5}

Valor de data/hora em formato Java™. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT, ou um valor de string de data/hora com um dos seguintes formatos:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* está no intervalo de 0 a 23.

*[!DNL zzz]* é um código de fuso horário com três ou quatro caracteres, como &quot;GMT&quot; ou &quot;PST&quot;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &quot;PST&quot; para o Horário padrão do Pacífico, versus &quot;PDT&quot; para o Horário de verão do Pacífico).

*[!DNL offset]* é uma diferença de fuso horário em horas ou horas:minutes, relativa a GMT. Por exemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados em sequência devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *[!DNL catalog]*.ini] será usada em seu lugar.

## Padrão {#section-65fb29a9ea2044df8cb9fe295eb14872}

Se estiver vazio ou não definido, o servidor usa a hora de modificação deste arquivo [!DNL *[!DNL catalog]*.ini].

## Consulte também {#section-764188f9b1734ad1a6270f5fecd28532}

[catálogo::CarimboHora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vinheta::CarimboHora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [atributo::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)

