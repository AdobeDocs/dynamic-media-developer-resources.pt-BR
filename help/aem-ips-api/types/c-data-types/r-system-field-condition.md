---
description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
solution: Experience Manager
title: CondiçãoCampoSistema
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 0%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Uma condição de pesquisa de campo do sistema para a operação searchAssets.

Para comparações unárias, passe exatamente um valor ( `boolVal`, `longVal`, `doubleVal` ou `dateVal`), dependendo do tipo de campo do sistema. Para intervalos de pesquisa, passe os parâmetros `min<Type>` e `max<Type>` e passe um valor `op` de `Between` ou `NotBetween`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| campo | `xsd:string` | Escolha de Campos do sistema de pesquisa de ativos. |
| op | `xsd:string` | Escolha de Operadores de Comparação de String. |
| value | `xsd:string` | Valor para testar. |
| boolVal | `xsd:boolean` | Valor de comparação booleano. |
| longVal | `xsd:long` | Valor de comparação longo. |
| minLong | `xsd:long` | Limite inferior do intervalo longo. |
| maxLong | `xsd:long` | Limite superior da faixa longa. |
| doubleVal | `xsd:double` | Valor de comparação duplo. |
| minDouble | `xsd:double` | Limite inferior do intervalo duplo. |
| maxDouble | `xsd:double` | Limite superior do intervalo duplo. |
| dateVal | `xsd:dateTime` | Valor de comparação de datas. |
| minDate | `xsd:dateTime` | Intervalo de datas mínimo. |
| maxDate | `xsd:dateTime` | Intervalo de datas máximo. |

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

