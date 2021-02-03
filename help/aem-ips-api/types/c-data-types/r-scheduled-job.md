---
description: Um trabalho programado para execução.
seo-description: Um trabalho programado para execução.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Dynamic Media Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# ScheduledJob{#scheduledjob}

Um trabalho programado para execução.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Alça da empresa. |
| `*`jobHandle`*` | `xsd:string` | Manuseio de trabalho agendado. |
| `*`name`*` | `xsd:string` | Nome do trabalho. |
| `*`originalName`*` | `xsd:string` | Nome original do trabalho agendado. |
| `*`type`*` | `xsd:string` | Tipo de tarefa. |
| `*`submitUserEmail`*` | `xsd:string` | O endereço de email do usuário que agendou o trabalho. |
| `*`locale`*` | `xsd:string` | A localidade a ser usada para detalhes do registro de tarefas e localização de e-mail. As localidades são especificadas como `<language_code>[- <country_code>]`, onde o código de idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código de país opcional é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166. Por exemplo, a string de localidade para inglês (Estados Unidos) seria: `en-US`. |
| `*`descrição`*` | `xsd:string` | Uma descrição do trabalho conforme especificado originalmente em `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Quando a tarefa estiver programada para execução. |
| `*`nextFireTime`*` | `xsd:dateTime` | A data, a hora e o fuso horário em que o trabalho será acionado. |
| `*`timeZone`*` | `xsd:dateTime` | O fuso horário do trabalho agendado. |
| `*`triggerState`*` | `xsd:int` | Estado do acionador da escolha de trabalho. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Detalhes da tarefa para uma tarefa de publicação de serviço de imagem. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Detalhes do trabalho para um trabalho de renderização de imagem. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Detalhes do trabalho para um trabalho de publicação de vídeo. Consulte [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Detalhes da tarefa para uma tarefa de publicação de diretório de servidor. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Detalhes do trabalho para um trabalho de diretório de upload. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Detalhes do trabalho para um trabalho de upload de URLs. |
| `*`otimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Permitir exportação autorizada de arquivos carregados anteriormente. Consulte [Exportar trabalho](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando você especifica um valor de tipo de trabalho em `submitJob`, o sistema retorna um trabalho com base nesse tipo. Os seguintes trabalhos podem ser retornados:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

