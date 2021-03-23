---
description: Uma tarefa agendada para execução.
seo-description: Uma tarefa agendada para execução.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# ScheduledJob{#scheduledjob}

Uma tarefa agendada para execução.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Manuseio da empresa. |
| `*`jobHandle`*` | `xsd:string` | Manuseio de trabalho agendado. |
| `*`name`*` | `xsd:string` | Nome da tarefa. |
| `*`originalName`*` | `xsd:string` | Nome original do trabalho agendado. |
| `*`type`*` | `xsd:string` | Tipo de tarefa. |
| `*`submitUserEmail`*` | `xsd:string` | O endereço de email do usuário que agendou o trabalho. |
| `*`locale`*` | `xsd:string` | A localidade a ser usada para detalhes do log de tarefas e localização de email. As localidades são especificadas como `<language_code>[- <country_code>]`, onde o código de idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código de país opcional é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166. Por exemplo, a sequência de caracteres da localidade para inglês (Estados Unidos) seria: `en-US`. |
| `*`descrição`*` | `xsd:string` | Uma descrição da tarefa conforme especificado originalmente em `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Quando a tarefa estiver agendada para execução. |
| `*`nextFireTime`*` | `xsd:dateTime` | A data, a hora e o fuso horário em que a tarefa será acionada. |
| `*`timeZone`*` | `xsd:dateTime` | O fuso horário do trabalho agendado. |
| `*`triggerState`*` | `xsd:int` | Estado do gatilho de escolha de trabalho. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Detalhes do trabalho para um trabalho de publicação de fornecimento de imagem. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Detalhes do trabalho para um trabalho de renderização de imagem. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Detalhes do trabalho para um trabalho de publicação de vídeo. Consulte [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Detalhes do trabalho para um trabalho de publicação do diretório do servidor. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Detalhes do trabalho para um trabalho de diretório de upload. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Detalhes do trabalho para um trabalho de upload de URLs. |
| `*`otimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Permitir exportação autorizada de arquivos carregados anteriormente. Consulte [Exportar Trabalho](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando você especifica um valor de tipo de trabalho em `submitJob`, o sistema retorna uma tarefa com base nesse tipo. As seguintes tarefas podem ser retornadas:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

