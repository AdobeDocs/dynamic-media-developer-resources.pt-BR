---
description: Agrupar arquivos em conjuntos usando uma matriz de lista de identificadores de ativos.
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
TQID: 'https://experienceleague.adobe.com/YHElzYMAYDta1hG2th30GNuz2IgFmN5OTUPx63K1p9o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

Agrupar arquivos em conjuntos usando uma matriz de lista de identificadores de ativos.

Sintaxe

## Parâmetros {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3">Uma matriz de manipuladores de ativos usados para criar o conjunto. <p>Por padrão, 1000 é o número máximo de ativos que você pode ter na matriz. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Caminho para a pasta onde deseja salvar os conjuntos. Salva na pasta raiz da empresa por padrão. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Define um sinalizador para indicar se os ativos devem ser publicados ou não. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Uma matriz de scripts de geração definidos que você pode executar nos arquivos carregados. Consulte <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configure uma notificação por email automática para o trabalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Opções de emailSetting**

O parâmetro `emailSetting` inclui as seguintes opções:

| Opção | Devoluções |
|---|---|
| `All` | Todas as notificações de tarefas (erros, avisos, conclusão) para o recipient especificado. |
| `Error` | Erros de trabalho para o destinatário especificado. |
| `ErrorAndWarning` | Erros e avisos de trabalho para o destinatário especificado. |
| `JobCompletion` | Uma notificação de conclusão de tarefa para o recipient especificado. |
| `None` | O trabalho não envia notificações ao destinatário especificado. |

## Exemplo {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

