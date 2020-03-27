---
description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
seo-description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
seo-title: CondiçãoCampoSistema
solution: Experience Manager
title: CondiçãoCampoSistema
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CondiçãoCampoSistema{#systemfieldcondition}

Uma condição de pesquisa de campo do sistema para a operação searchAssets.

Para comparação unária, passe exatamente um valor ( `boolVal`, `longVal`, `doubleVal`ou `dateVal`) dependendo do tipo de campo do sistema. Para intervalos de pesquisa, passe `min<Type>` e `max<Type>` parâmetros e transmita um `op` valor de `Between` ou `NotBetween`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`campo`*` | `xsd:string` | Escolha dos campos do sistema de pesquisa de ativos. |
| ` *`op`*` | `xsd:string` | Escolha dos operadores de comparação de sequências de caracteres. |
| ` *`value`*` | `xsd:string` | Valor a ser testado. |
| ` *`boolVal`*` | `xsd:boolean` | Valor de comparação booliano. |
| ` *`longVal`*` | `xsd:long` | Valor de comparação longo. |
| ` *`minLong`*` | `xsd:long` | Limite inferior de longo alcance. |
| ` *`maxLong`*` | `xsd:long` | Limite superior do intervalo longo. |
| ` *`doubleVal`*` | `xsd:double` | Valor de comparação do Duplo. |
| ` *`minDouble`*` | `xsd:double` | Limite inferior do intervalo do duplo. |
| ` *`maxDouble`*` | `xsd:double` | Limite superior do intervalo do duplo. |
| ` *`dateVal`*` | `xsd:dateTime` | Valor de comparação de data. |
| ` *`minDate`*` | `xsd:dateTime` | Intervalo de datas mínimo. |
| ` *`maxDate`*` | `xsd:dateTime` | Máximo de intervalo de datas. |

## Example {#section-347d4aabfff44530adba03d1dc0b9968}

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

