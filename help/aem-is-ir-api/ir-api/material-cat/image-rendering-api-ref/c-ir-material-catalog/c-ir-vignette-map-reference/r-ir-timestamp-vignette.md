---
description: Carimbo de data e hora da modificação. Especifica a data/hora em que a vinheta foi modificada pela última vez.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# TimeStamp{#timestamp}

Carimbo de data e hora da modificação. Especifica a data/hora em que a vinheta foi modificada pela última vez.

If `attribute::UseLastModified` for definida, a mais recente `vignette::TimeStamp` e `catalog::TimeStamp`o valor da vinheta e todos os materiais envolvidos na solicitação são retornados na resposta HTTP como um cabeçalho modificado pela última vez.

>[!NOTE]
>
>A hora real do arquivo da vinheta nunca é usada para essa finalidade.

`catalog::TimeStamp` também é usada para validação de cache baseada em catálogo (consulte [atributo::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propriedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de data/hora no formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* está no intervalo de 0 a 23.
* *[!DNL zzz]* é um código de fuso horário de 3 ou 4 caracteres, como &#39;GMT&#39; ou &#39;PST&#39;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &#39;PST&#39; para o horário padrão do Pacífico, versus &#39;PDT&#39; para o horário de verão do Pacífico).
* *[!DNL offset]* é um deslocamento de fuso horário em horas ou horas:minutos, em relação ao GMT. Por exemplo, &#39;PDT&#39; é equivalente a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados na string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do [!DNL *[!DNL catalog]*.ini] arquivo é usado em vez disso.

## Padrão {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` é o campo que está vazio ou não está presente.

## Consulte também {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
