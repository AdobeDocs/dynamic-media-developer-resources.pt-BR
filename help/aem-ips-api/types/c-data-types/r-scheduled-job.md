---
description: Um trabalho programado para ser executado.
solution: Experience Manager
title: Trabalho Agendado
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 276
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
| localidade | `xsd:string` | A localidade a ser usada para detalhes do log de trabalho e localização do email. As localidades são especificadas como `<language_code>[- <country_code>]`, onde o código do idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código opcional do país é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166. Por exemplo, a cadeia de caracteres local para inglês (Estados Unidos) seria: `en-US`. |
| descrição | `xsd:string` | Uma descrição do trabalho conforme originalmente especificado em `submitJob`. |
| execSchedule | `xsd:string` | Quando o trabalho está programado para ser executado. |
| nextFireTime | `xsd:dateTime` | A data, hora e fuso horário em que o trabalho é acionado. |
| timeZone | `xsd:dateTime` | O fuso horário do trabalho agendado. |
| triggerState | `xsd:int` | Escolha do estado do acionador do trabalho. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Detalhes de um trabalho de publicação de servidor de imagens. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Detalhes do trabalho para um trabalho de renderização de imagem. |
| videoPublishJob | `types:VideoPublishJob` | Detalhes de um trabalho de publicação de vídeo. Consulte [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=pt-BR). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Detalhes do trabalho de publicação de um diretório de servidor. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Detalhes do job para um job do diretório de upload. |
| uploadUrlsJob | `types:UploadUrlsJob` | Detalhes do trabalho para um trabalho de URLs de upload. |
| otimizeImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Permitir exportação autorizada de arquivos carregados anteriormente. Consulte [Exportar Trabalho](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=pt-BR). |

## Notas {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando você especifica um valor de tipo de trabalho em `submitJob`, o sistema retorna um trabalho com base nesse tipo. As seguintes tarefas podem ser retornadas:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
