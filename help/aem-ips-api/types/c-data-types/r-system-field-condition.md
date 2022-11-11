---
description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
solution: Experience Manager
title: CondiçãoCampoSistema
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Uma condição de pesquisa de campo do sistema para a operação searchAssets.

Para comparações unárias, passe exatamente um valor ( `boolVal`, `longVal`, `doubleVal`ou `dateVal`) dependendo do tipo de campo do sistema. Para intervalos de pesquisa, passe `min<Type>` e `max<Type>` e transmita um `op` valor de `Between` ou `NotBetween`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| campo | `xsd:string` | Opção de campos do sistema de pesquisa de ativos. |
| op | `xsd:string` | Escolha dos operadores de comparação de sequências de caracteres. |
| value | `xsd:string` | Valor para testar. |
| boolVal | `xsd:boolean` | Valor de comparação booleano. |
| longVal | `xsd:long` | Valor de comparação longo. |
| minLong | `xsd:long` | Limite inferior de longo alcance. |
| maxLong | `xsd:long` | Limite superior do intervalo longo. |
| doubleVal | `xsd:double` | Valor de comparação duplo. |
| minDouble | `xsd:double` | Limite inferior do intervalo duplo. |
| maxDouble | `xsd:double` | Limite superior do intervalo duplo. |
| dateVal | `xsd:dateTime` | Valor de comparação de data. |
| minDate | `xsd:dateTime` | Mínimo do intervalo de datas. |
| maxDate | `xsd:dateTime` | Máximo do intervalo de datas. |

## Exemplo {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```
