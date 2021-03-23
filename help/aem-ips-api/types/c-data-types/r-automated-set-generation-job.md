---
description: Agrupe arquivos em conjuntos usando uma matriz de lista do identificador de ativos.
seo-description: Agrupe arquivos em conjuntos usando uma matriz de lista do identificador de ativos.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Agrupe arquivos em conjuntos usando uma matriz de lista do identificador de ativos.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3">Uma matriz de identificadores de ativos usada para criar o conjunto. <p>Por padrão, 1000 é o número máximo de ativos que você pode ter na matriz. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Caminho para a pasta onde deseja salvar os conjuntos. Salva na pasta raiz da empresa por padrão. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Define um sinalizador para indicar se os ativos devem ser publicados ou não. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Uma matriz de scripts de geração de conjunto que podem ser executados nos arquivos carregados. Consulte <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configure uma notificação de email automatizada para a tarefa. </p> </td> 
  </tr> 
 </tbody> 
</table>

**opções de emailSetting**

O parâmetro `emailSetting` inclui as seguintes opções:

| Opção | Devoluções |
|---|---|
| `All` | Todas as notificações de trabalho (erros, avisos, conclusão) para o recipient especificado. |
| `Error` | Erros de tarefa para o recipient especificado. |
| `ErrorAndWarning` | Erros de tarefa e avisos para o recipient especificado. |
| `JobCompletion` | Uma notificação de conclusão de trabalho para o recipient especificado. |
| `None` | O trabalho não envia notificações de trabalho para o recipient especificado. |

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

