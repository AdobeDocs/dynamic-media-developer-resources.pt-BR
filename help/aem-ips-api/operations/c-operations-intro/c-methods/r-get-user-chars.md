---
description: Obtém uma lista dos caracteres usados em um campo específico.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '174'
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
| charField | `xsd:string` | Sim | Determina o Estado da lixeira a ser procurado. |
| includeInative | `xsd:boolean` | Sim | Incluir ou excluir usuários inativos. Usuários não administrativos do IPS devem ser membros ativos de pelo menos uma empresa para serem autorizados a fazer chamadas de API. Uma falha de autorização é retornada se o usuário não tiver associações ativas à empresa. |
| includeInvalid | `xsd:boolean` | Não | Incluir ou excluir usuários inválidos. |
| companyHandleArray | `types:HandleArray` | Não | Filtre os resultados com base na empresa. |
| groupHandleArray | `types:HandleArray` | Não | Filtra os resultados com base em grupos. |
| userRoleArray | `types:StringArray` | Não | Filtra os resultados com base na função do usuário. |
| numChars | `xsd:int` | Não | Habilitar > 1 caractere. |

**Saída (getUserCharsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Sim | Uma matriz de prefixos de caracteres. |

## Exemplos {#section-3702f165e8b041139a6144f4a76ca25f}

Este exemplo de código retorna:

* Primeiros caracteres dos últimos nomes dos usuários de uma empresa específica.
* Um conjunto de grupos.
* Um conjunto de funções de usuário.

A constante de string Campos de filtro de caractere do usuário determina o tipo de caracteres do usuário retornados.

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
