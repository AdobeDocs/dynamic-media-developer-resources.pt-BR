---
description: Carimbo de data e hora da modificação. Especifica a data/hora em que a vinheta foi modificada pela última vez.
seo-description: Carimbo de data e hora da modificação. Especifica a data/hora em que a vinheta foi modificada pela última vez.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Carimbo de data e hora da modificação. Especifica a data/hora em que a vinheta foi modificada pela última vez.

Se `attribute::UseLastModified` for definido, o valor mais recente `vignette::TimeStamp` e `catalog::TimeStamp`da vinheta e todos os materiais envolvidos na solicitação serão retornados na resposta HTTP como um cabeçalho modificado pela última vez.

>[!NOTE]
>
>A hora real do arquivo da vinheta nunca é usada para essa finalidade.

`catalog::TimeStamp` também é usada para validação de cache baseada em catálogo (consulte  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propriedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de data/hora no formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* está no intervalo de 0 a 23.
* *[!DNL zzz]* é um código de fuso horário de 3 ou 4 caracteres, como &#39;GMT&#39; ou &#39;PST&#39;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &#39;PST&#39; para o horário padrão do Pacífico, versus &#39;PDT&#39; para o horário de verão do Pacífico).
* *[!DNL offset]* é um deslocamento de fuso horário em horas ou horas:minutos, em relação ao GMT. Por exemplo, &#39;PDT&#39; é equivalente a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados na string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *[!DNL catalog]*.ini] será usada.

## Padrão {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` é o campo que está vazio ou não está presente.

## Consulte também {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
