---
description: Obtém uma lista dos caracteres usados em um campo específico.
seo-description: Obtém uma lista dos caracteres usados em um campo específico.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Dynamic Media Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# getUserChars{#getuserchars}

Obtém uma lista dos caracteres usados em um campo específico.

Sintaxe

## Tipos de usuário autorizados {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Entrada (getUserCharsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | Sim | Determina o Estado de lixeira a ser pesquisado. |
| `*`includeInative`*` | `xsd:boolean` | Sim | Incluir ou excluir usuários inativos. Usuários administradores não IPS devem ser membros ativos de pelo menos uma empresa para serem autorizados a fazer chamadas de API. Uma falha de autorização será retornada se o usuário não tiver associações de empresa ativas. |
| `*`includeInvalid`*` | `xsd:boolean` | Não | Incluir ou excluir usuários inválidos. |
| `*`companyHandleArray`*` | `types:HandleArray` | Não | Filtre os resultados com base na empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | Não | Resultados de filtros com base em grupos. |
| `*`userRoleArray`*` | `types:StringArray` | Não | Resultados de filtros com base na função do usuário. |
| `*`numChars`*` | `xsd:int` | Não | Habilitar > 1 caractere. |

**Saída (getUserCharsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Sim | Uma matriz de prefixos de caracteres. |

## Exemplos {#section-3702f165e8b041139a6144f4a76ca25f}

Este exemplo de código retorna:

* Os primeiros caracteres dos sobrenomes dos usuários de uma empresa específica.
* Um conjunto de grupos.
* Um conjunto de funções de usuário.

A constante de string Campos de Filtro de Caracteres do Usuário determina o tipo de caracteres do usuário retornados.

**Solicitação**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Resposta**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

