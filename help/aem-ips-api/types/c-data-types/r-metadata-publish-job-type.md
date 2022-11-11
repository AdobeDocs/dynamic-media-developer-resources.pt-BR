---
description: Publica metadados no servidor de metadados.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

Publica metadados no servidor de metadados.

Sintaxe

## Parâmetros {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Defina como <span class="codeph"> Verdadeiro</span> para publicar <i>all</i> dados para o servidor de metadados novamente. <p>Observação: Dependendo da quantidade de dados, isso pode levar de vários minutos a algumas horas. </p><p>Não defina esse parâmetro se quiser publicar somente metadados novos ou alterados. </p></td> 
  </tr> 
 </tbody> 
</table>
