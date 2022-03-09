---
description: Uma tarefa agendada para execução.
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# ScheduledJob{#scheduledjob}

Uma tarefa agendada para execução.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| companyHandle | `xsd:string` | Manuseio da empresa. |
| jobHandle | `xsd:string` | Manuseio de trabalho agendado. |
| name | `xsd:string` | Nome da tarefa. |
| originalName | `xsd:string` | Nome original do trabalho agendado. |
| type | `xsd:string` | Tipo de tarefa. |
| submitUserEmail | `xsd:string` | O endereço de email do usuário que agendou o trabalho. |
| locale | `xsd:string` | A localidade a ser usada para detalhes do log de tarefas e localização de email. As localidades são especificadas como `<language_code>[- <country_code>]`, em que o código linguístico é um código de duas letras em minúsculas, conforme especificado pela norma ISO-639, e o código opcional do país é um código de duas letras em maiúsculas, conforme especificado pela norma ISO-3166. Por exemplo, a sequência de caracteres da localidade para inglês (Estados Unidos) seria: `en-US`. |
| descrição | `xsd:string` | Uma descrição da tarefa conforme especificado originalmente em `submitJob`. |
| execSchedule | `xsd:string` | Quando a tarefa estiver agendada para execução. |
| nextFireTime | `xsd:dateTime` | A data, a hora e o fuso horário em que a tarefa é acionada. |
| timeZone | `xsd:dateTime` | O fuso horário do trabalho agendado. |
| triggerState | `xsd:int` | Estado do gatilho de escolha de trabalho. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Detalhes do trabalho para um trabalho de publicação de fornecimento de imagem. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Detalhes do trabalho para um trabalho de renderização de imagem. |
| videoPublishJob | `types:VideoPublishJob` | Detalhes do trabalho para um trabalho de publicação de vídeo. Consulte [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Detalhes do trabalho para um trabalho de publicação do diretório do servidor. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Detalhes do trabalho para um trabalho de diretório de upload. |
| uploadUrlsJob | `types:UploadUrlsJob` | Detalhes do trabalho para um trabalho de upload de URLs. |
| otimizeImagesJob | `types:OptimizeImagesJob` |  |
| ripPdfsJob | `types:RipPdfsJob` |  |
| reprocessAssetsJob | `types:ReprocessAssetsJob` |  |
| exportJob | `types:ExportJob` | Permitir exportação autorizada de arquivos carregados anteriormente. Consulte [Exportar trabalho](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Ao especificar um valor do tipo de tarefa em `submitJob`, o sistema retorna uma tarefa com base nesse tipo. As seguintes tarefas podem ser retornadas:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
