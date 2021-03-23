---
description: Envia uma tarefa para o sistema.
seo-description: Envia uma tarefa para o sistema.
seo-title: submitJob
solution: Experience Manager
title: submitJob
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# submitJob{#submitjob}

Envia uma tarefa para o sistema.

Sintaxe

## Tipos de usuário autorizados {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-31a07dbccf964850883e817384499459}

**Entrada (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Manuseio da empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Manipule o usuário que enviou o trabalho. </p> <p> <p>Observação: O sistema envia email para o usuário especificado por <span class="codeph"> userHandle</span>. Se <span class="codeph"> userHandle</span> não for fornecido, a pessoa que enviou o trabalho receberá os emails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Nome da tarefa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>A localidade usada para detalhes do log de tarefas e localização de email. </p> <p>As localidades são especificadas como <span class="codeph"> &lt;language_code&gt;</span> e <span class="codeph"> [&lt;country_code&gt;]</span>, onde o código de idioma é um código de duas letras em minúsculas, conforme especificado pela ISO-639, e o código de país opcional é um código de duas letras em maiúsculas, conforme especificado pela ISO-3166. Por exemplo, a sequência de caracteres da localidade para inglês (Estados Unidos) seria: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Data e hora para executar a tarefa. </p> <p>Observação:  Forneça o fuso horário com a solicitação. Os fusos horários são ajustados para o fuso horário do servidor IPS de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Determina quando executar a tarefa. </p> <p> Pode ser uma sequência <span class="codeph"> cron</span> que executa o trabalho de forma recorrente. </p> <p>O agendamento é sempre relativo ao fuso horário local do servidor. Consulte a documentação do IPS para ver o formato de agendamento personalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrição</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Descrição da tarefa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ExportJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Exportar arquivos carregados anteriormente. </p> <p>Consulte <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de publicação de fornecimento de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de publicação de renderização de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VideoPublishJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de publicação de vídeo. </p> <p>Consulte <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de publicação do diretório do servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de diretório de upload. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:UploadUrlsJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Detalhes de um trabalho de upload de URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> otimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:OtimizeImagesJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:RipPdfsJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automaticSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Processar uma lista de ativos em conjuntos usando Scripts de conjunto automatizado. </p> <p>Consulte <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (submitJobReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`jobHandle`*` | `xsd:string` | Sim | Identificador da tarefa. |

## Exemplos {#section-40ac77d14adf4588ba2575be6879b2d2}

Esta amostra de código envia um trabalho de publicação de fornecimento de imagem para o IPS e retorna um identificador de trabalho. Escolha apenas um tipo de trabalho na solicitação. Como `userHandle` foi omitido, as notificações por email são enviadas ao usuário que enviou o trabalho. Esta tarefa de amostra é executada imediatamente porque `execTime` e `execSchedule` foram omitidas.

**Solicitação**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Resposta**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Notas {#section-0f3078e503a249aeb6f3d662a51f036a}

Você pode especificar no máximo um de `execTime` e `execSchedule`. Se nenhum dos dois for aprovado, a tarefa será executada imediatamente. Você pode usar somente um dos seguintes:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

