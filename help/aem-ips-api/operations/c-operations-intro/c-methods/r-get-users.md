---
description: Obtém uma matriz de usuários, conforme especificado pelos manipuladores de empresa, grupo e função de usuário. Essa operação permite classificar usuários retornados e filtrar por caractere.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
TQID: 'https://experienceleague.adobe.com/17FQLNVfRg84FeVetVfuTWoLRMf8ugBwXBi2CpmLZfI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 0%

---

# getUsers{#getusers}

Obtém uma matriz de usuários, conforme especificado pelos manipuladores de empresa, grupo e função de usuário. Essa operação permite classificar usuários retornados e filtrar por caractere.

## Tipos de usuário autorizados {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| includeInative | `xsd:boolean` | Não | Incluir ou excluir usuários inativos. Os usuários não administradores de IPS devem ser membros ativos de pelo menos uma empresa para serem autorizados a fazer chamadas de API. Uma falha de autorização é retornada se o usuário não tiver associações ativas da empresa. |
| includeInvalid | `xsd:boolean` | Não | Permite incluir/excluir usuários inválidos. |
| companyHandleArray | `types:HandleArray` | Não | Filtrar resultados por empresa. |
| groupHandleArray | `types:HandleArray` | Não | Filtrar resultados por grupo. |
| userRoleArray | `types:StringArray` | Não | Filtrar resultados por função de usuário. |
| charFilterField | `xsd:string` | Não | Filtrar resultados pelo prefixo da cadeia de caracteres do campo (consulte [!DNL Trash State).] |
| charFilter | `xsd:string` | Não | Filtrar resultados por um caractere específico. |
| sortBy | `xsd:string` | Não | Escolha de campos de classificação do usuário. |
| recordsPerPage | `xsd:int` | Não | Retorna o número especificado de registros por página. |
| resultsPage | `xsd:int` | Não | Página de resultados. |

**Saída (getUsersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userArray | `types:UserArray` | Sim | Uma matriz de usuários. |

## Exemplos {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Esta amostra de código retorna a matriz de usuários para vários parâmetros opcionais. Funções de usuário, campos de filtro de caracteres do usuário e campos de classificação do usuário são determinados com o uso de Constantes de String específicas.

**Solicitação**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Resposta**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
