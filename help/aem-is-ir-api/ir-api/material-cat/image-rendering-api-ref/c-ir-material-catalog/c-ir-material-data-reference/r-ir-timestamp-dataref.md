---
description: Carimbo de data e hora da modificação do arquivo. Especifica a data/hora em que a imagem e/ou os arquivos de dados anexados a este registro de catálogo foram modificados pela última vez.
seo-description: Carimbo de data e hora da modificação do arquivo. Especifica a data/hora em que a imagem e/ou os arquivos de dados anexados a este registro de catálogo foram modificados pela última vez.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Carimbo de data e hora da modificação do arquivo. Especifica a data/hora em que a imagem e/ou os arquivos de dados anexados a este registro de catálogo foram modificados pela última vez.

Se `attribute::UseLastModified` for definido, o mais recente dos valores `catalog::TimeStamp` e `vignette::TimeStamp` de todos os materiais e a vinheta envolvida na solicitação será retornada na resposta HTTP como um cabeçalho modificado pela última vez.

>[!NOTE]
>
>Os tempos de arquivo reais da imagem ou dos arquivos de dados anexados a esse registro de catálogo nunca são usados para essa finalidade.

`catalog::TimeStamp` também é usada para validação de cache baseada em catálogo (consulte  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propriedades {#section-42f09e375e72492b87a3a486da7df808}

Valor de data/hora no formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* está no intervalo de 0 a 23.
* *[!DNL zzz]* é um código de fuso horário de 3 ou 4 caracteres, como &#39;GMT&#39; ou &#39;PST&#39;. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, &#39;PST&#39; para o horário padrão do Pacífico, versus &#39;PDT&#39; para o horário de verão do Pacífico).
* *[!DNL offset]* é um deslocamento de fuso horário em horas ou horas:minutos, em relação ao GMT. Por exemplo, &#39;PDT&#39; é equivalente a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados na string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo *catalog*.ini será usada.

## Padrão {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` é o campo que está vazio ou não está presente.

## Consulte também {#section-876f1d1b50dc4501b605820015a29451}

[atributo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [atributo::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [atributo: CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [vinheta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
