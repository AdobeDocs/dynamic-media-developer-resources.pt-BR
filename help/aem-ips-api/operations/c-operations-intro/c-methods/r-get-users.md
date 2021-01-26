---
description: Obtém uma matriz de usuários, conforme especificado pelas manipulações de função de empresa, grupo e usuário. Essa operação permite que você classifique os usuários retornados e filtre por caractere.
seo-description: Obtém uma matriz de usuários, conforme especificado pelas manipulações de função de empresa, grupo e usuário. Essa operação permite que você classifique os usuários retornados e filtre por caractere.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Dynamic Media Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# getUsers{#getusers}

Obtém uma matriz de usuários, conforme especificado pelas manipulações de função de empresa, grupo e usuário. Essa operação permite que você classifique os usuários retornados e filtre por caractere.

## Tipos de usuário autorizados {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`includeInative`*` | `xsd:boolean` | Não | Incluir ou excluir usuários inativos. Usuários administradores não IPS devem ser membros ativos de pelo menos uma empresa para serem autorizados a fazer chamadas de API. Uma falha de autorização será retornada se o usuário não tiver associações de empresa ativas. |
| `*`includeInvalid`*` | `xsd:boolean` | Não | Permite incluir/excluir usuários inválidos. |
| `*`companyHandleArray`*` | `types:HandleArray` | Não | Filtre os resultados por empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | Não | Filtrar resultados por grupo. |
| `*`userRoleArray`*` | `types:StringArray` | Não | Filtre os resultados por função de usuário. |
| `*`charFilterField`*` | `xsd:string` | Não | Filtrar resultados por prefixo de string do campo (consulte [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | Não | Filtre os resultados por um caractere específico. |
| `*`sortBy`*` | `xsd:string` | Não | Escolha dos campos de classificação do usuário. |
| `*`recordsPerPage`*` | `xsd:int` | Não | Retorna o número especificado de registros por página. |
| `*`resultsPage`*` | `xsd:int` | Não | Página de resultados. |

**Saída (getUsersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Sim | Uma matriz de usuários. |

## Exemplos {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Essa amostra de código retorna a matriz de usuários para vários parâmetros opcionais. As funções do usuário, os campos de filtro de caractere do usuário e os campos de classificação do usuário são determinados usando Constantes de string específicas.

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

