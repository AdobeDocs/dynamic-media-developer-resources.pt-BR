---
description: Atualiza os valores do dicionário de tags para um campo de tag.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# updateTagFieldValues{#updatetagfieldvalues}

Atualiza os valores do dicionário de tags para um campo de tag.

Sintaxe

## Tipos de usuário autorizados {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-0a3a4bab026746238c9d4009caf42e94}

**Entrada (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Manuseio da empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Identificador de campo de tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4">Matriz de valores de campo de tag que você deseja atualizar. <p>Observação:  Atualiza somente os valores da string de tag. Não afeta associações de ativos. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (updateTagFieldValuesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | O número de campos de tag atualizados com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou atualizar campos de tag. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou atualizar campos de tag. |
| `*`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou atualizar campos de tag. |
| `*`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou atualizar campos de tag. |

## Exemplos {#section-bb4dcf97044c4675974c9b8d27674001}

**Solicitação**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Resposta**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

