---
title: Carimbo de data/hora
description: Carimbo de data/hora de modificação. Especifica a data/hora da última modificação desta vinheta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Carimbo de data/hora{#timestamp}

Carimbo de data/hora de modificação. Especifica a data/hora da última modificação desta vinheta.

Se `attribute::UseLastModified` estiver definido, o `vignette::TimeStamp` e o `catalog::TimeStamp` mais recentes da vinheta e todos os materiais envolvidos na solicitação serão retornados na resposta HTTP como um cabeçalho de última modificação.

>[!NOTE]
>
>A hora real do arquivo de vinheta nunca é usada para essa finalidade.

O `catalog::TimeStamp` também é usado para validação de cache com base em catálogo. Consulte [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propriedades {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valor de data/hora em formato Java™. Pode ser o número inteiro de milissegundos desde meia-noite, 1º de janeiro de 1970 UTC/GMT, ou um valor de string de data/hora com um dos seguintes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* está no intervalo 0-23.
* *[!DNL zzz]* é um código de fuso horário com três ou quatro caracteres, como &quot;GMT&quot; ou &quot;PST&quot;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &quot;PST&quot; para o Horário padrão do Pacífico, versus &quot;PDT&quot; para o Horário de verão do Pacífico).
* *[!DNL offset]* é uma diferença de fuso horário em horas ou horas:minutos, relativa a GMT. Por exemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados em sequência devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *[!DNL catalog]*.ini] será usada em seu lugar.

## Padrão {#section-562c221d2e8b4a97ab5e9a3605f22140}

O `attribute::TimeStamp` é o campo vazio ou ausente.

## Consulte também {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
