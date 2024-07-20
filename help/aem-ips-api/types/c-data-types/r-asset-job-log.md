---
title: AssetJobLog
description: Os detalhes de uma entrada do log de trabalho associada a um ativo específico. Dados retornados por getAssetJobLogs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# [!DNL AssetJobLog]{#assetjoblog}

Os detalhes de uma entrada do log de trabalho associada a um ativo específico. Dados retornados por getAssetJobLogs.

Sintaxe

## Parâmetros {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador do trabalho. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome da tarefa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logMessage]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Mensagem no log do trabalho. <p>O campo de resposta <span class="codeph"> [!DNL logMessage]</span> foi localizado com base no campo de localidade <span class="codeph"> authHeader</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tipo de trabalho na entrada do log. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL submitUserEmail]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> e-mail do usuário que enviou o job. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logDate]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data do trabalho. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL auxArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:JobLogDetailArray</span> </td> 
   <td colname="col3"> Matriz de mensagens de log de trabalho auxiliar para cada log de trabalho. </td> 
  </tr> 
 </tbody> 
</table>
