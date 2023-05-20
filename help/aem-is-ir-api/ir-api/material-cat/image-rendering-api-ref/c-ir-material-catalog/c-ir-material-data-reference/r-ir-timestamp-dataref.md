---
description: Carimbo de data/hora de modificação de arquivo. Especifica a data/hora em que os arquivos de imagem e/ou de dados anexados a esse registro de catálogo foram modificados pela última vez.
solution: Experience Manager
title: Carimbo de data/hora
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Carimbo de data/hora{#timestamp}

Carimbo de data/hora de modificação de arquivo. Especifica a data/hora em que os arquivos de imagem e/ou de dados anexados a esse registro de catálogo foram modificados pela última vez.

Se `attribute::UseLastModified` estiver definido, o mais recente dos `catalog::TimeStamp` e `vignette::TimeStamp` Os valores de todos os materiais e a vinheta envolvida na solicitação são retornados na resposta HTTP como um cabeçalho modificado por último.

>[!NOTE]
>
>Os horários reais dos arquivos de imagem ou de dados anexados a esse registro de catálogo nunca são usados para essa finalidade.

`catalog::TimeStamp` também é usado para validação de cache baseada em catálogo (consulte [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propriedades {#section-42f09e375e72492b87a3a486da7df808}

Valor de data/hora em formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* está no intervalo de 0 a 23.
* *[!DNL zzz]* é um código de fuso horário de 3 ou 4 caracteres, como &quot;GMT&quot; ou &quot;PST&quot;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &quot;PST&quot; para o Horário padrão do Pacífico, versus &quot;PDT&quot; para o Horário de verão do Pacífico).
* *[!DNL offset]* é um deslocamento de fuso horário em horas ou horas:minutos, em relação a GMT. Por exemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados com string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do *catálogo* em vez disso, é usado o arquivo .ini.

## Padrão {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` é o campo está vazio ou não está presente.

## Consulte também {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vinheta::Carimbo de data/hora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
