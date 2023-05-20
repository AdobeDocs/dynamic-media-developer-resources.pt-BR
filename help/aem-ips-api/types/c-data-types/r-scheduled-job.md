---
description: Um trabalho programado para ser executado.
solution: Experience Manager
title: Trabalho Agendado
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# [!DNL ScheduledJob]{#scheduledjob}

Um trabalho programado para ser executado.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| companyHandle | `xsd:string` | Identificador da empresa. |
| jobHandle | `xsd:string` | Identificador de trabalho agendado. |
| name | `xsd:string` | Nome do trabalho. |
| originalName | `xsd:string` | Nome original do trabalho agendado. |
| type | `xsd:string` | Tipo de trabalho. |
| submitUserEmail | `xsd:string` | O endereço de email do usuário que agendou o trabalho. |
| localidade | `xsd:string` | A localidade a ser usada para detalhes do log de trabalho e localização do email. As localidades são especificadas como `<language_code>[- <country_code>]`, em que o código de idioma é um código de duas letras em minúsculas, conforme especificado pela norma ISO-639, e o código opcional de país é um código de duas letras em maiúsculas, conforme especificado pela norma ISO-3166. Por exemplo, a sequência de caracteres do local para inglês (Estados Unidos) seria: `en-US`. |
| descrição | `xsd:string` | Uma descrição do processo, conforme especificado originalmente em `submitJob`. |
| execSchedule | `xsd:string` | Quando o trabalho está programado para ser executado. |
| nextFireTime | `xsd:dateTime` | A data, hora e fuso horário em que o trabalho é acionado. |
| timeZone | `xsd:dateTime` | O fuso horário do trabalho agendado. |
| triggerState | `xsd:int` | Escolha do estado do acionador do trabalho. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Detalhes de um trabalho de publicação de servidor de imagens. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Detalhes do trabalho para um trabalho de renderização de imagem. |
| videoPublishJob | `types:VideoPublishJob` | Detalhes de um trabalho de publicação de vídeo. Consulte [TrabalhoDePublicaçãoDeVídeo](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Detalhes do trabalho de publicação de um diretório de servidor. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Detalhes do job para um job do diretório de upload. |
| uploadUrlsJob | `types:UploadUrlsJob` | Detalhes do trabalho para um trabalho de URLs de upload. |
| otimizeImagesJob | `types:OptimizeImagesJob` |  |
| ripPdfsJob | `types:RipPdfsJob` |  |
| reprocessAssetsJob | `types:ReprocessAssetsJob` |  |
| exportJob | `types:ExportJob` | Permitir exportação autorizada de arquivos carregados anteriormente. Consulte [Exportar tarefa](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando você especifica um valor de tipo de trabalho em `submitJob`, o sistema retorna um trabalho com base nesse tipo. As seguintes tarefas podem ser retornadas:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
