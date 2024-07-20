---
description: Envia um processo ao sistema.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# submitJob{#submitjob}

Envia um processo ao sistema.

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
   <td colname="col4"> <p>Identificador da empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Processe o usuário que enviou o job. </p> <p> <p>Observação: o sistema envia um email ao usuário especificado por <span class="codeph"> userHandle</span>. Se <span class="codeph"> userHandle</span> não for fornecido, a pessoa que enviou o trabalho receberá os emails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Nome do trabalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> localidade</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>A localidade usada para detalhes do log de trabalho e localização do email. </p> <p>As localidades estão especificadas como <span class="codeph"> &lt;código_idioma&gt;</span> e <span class="codeph"> [&lt;código_país&gt;]</span>, onde o código de idioma é em minúsculas, código de duas letras, conforme especificado por ISO-639, e o código opcional de país é em maiúsculas, código de duas letras, conforme especificado por ISO-3166. Por exemplo, a sequência de caracteres do local para inglês (Estados Unidos) seria: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Data e hora de execução do job. </p> <p>Observação: forneça o fuso horário com a solicitação. Os fusos horários são ajustados ao fuso horário do servidor IPS de destino. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Determina quando executar a tarefa. </p> <p> Pode ser uma cadeia de caracteres <span class="codeph"> cron</span> que executa o trabalho de forma recorrente. </p> <p>O agendamento é sempre relativo ao fuso horário local do servidor. Consulte a documentação de IPS para obter o formato de agendamento personalizado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> descrição</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Descrição do trabalho. </p> </td> 
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
   <td colname="col4"> <p>Detalhes de um trabalho de publicação do servidor de imagens. </p> </td> 
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
   <td colname="col4"> <p>Detalhes de um trabalho de publicação de diretório de servidor. </p> </td> 
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
   <td colname="col4"> <p>Detalhes de um trabalho de URL de upload. </p> </td> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Processar uma lista de ativos em conjuntos usando Scripts de conjunto automatizados. </p> <p>Consulte <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (submitJobReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| jobHandle | `xsd:string` | Sim | Identificador do trabalho. |

## Exemplos {#section-40ac77d14adf4588ba2575be6879b2d2}

Esta amostra de código envia um trabalho de publicação de servidor de imagens para o IPS e retorna um identificador de trabalho. Escolha apenas um tipo de trabalho na solicitação. Como `userHandle` foi omitido, notificações por email são enviadas ao usuário que enviou o trabalho. Este trabalho de exemplo é executado imediatamente porque `execTime` e `execSchedule` foram omitidos.

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

Você pode especificar no máximo `execTime` e `execSchedule`. Se nenhum for aprovado, o job será executado imediatamente. Você pode usar apenas um dos seguintes:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
