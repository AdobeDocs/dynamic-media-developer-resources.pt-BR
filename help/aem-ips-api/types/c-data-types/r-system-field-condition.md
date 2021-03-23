---
description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
seo-description: Uma condição de pesquisa de campo do sistema para a operação searchAssets.
seo-title: CondiçãoCampoSistema
solution: Experience Manager
title: CondiçãoCampoSistema
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# CondiçãoCampoSistema{#systemfieldcondition}

Uma condição de pesquisa de campo do sistema para a operação searchAssets.

Para comparações unárias, passe exatamente um valor ( `boolVal`, `longVal`, `doubleVal` ou `dateVal`), dependendo do tipo de campo do sistema. Para intervalos de pesquisa, passe os parâmetros `min<Type>` e `max<Type>` e transmita um valor `op` `Between` ou `NotBetween`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`campo`*` | `xsd:string` | Opção de campos do sistema de pesquisa de ativos. |
| `*`op`*` | `xsd:string` | Escolha dos operadores de comparação de sequências de caracteres. |
| `*`value`*` | `xsd:string` | Valor para testar. |
| `*`boolVal`*` | `xsd:boolean` | Valor de comparação booleano. |
| `*`longVal`*` | `xsd:long` | Valor de comparação longo. |
| `*`minLong`*` | `xsd:long` | Limite inferior de longo alcance. |
| `*`maxLong`*` | `xsd:long` | Limite superior do intervalo longo. |
| `*`doubleVal`*` | `xsd:double` | Valor de comparação duplo. |
| `*`minDouble`*` | `xsd:double` | Limite inferior do intervalo duplo. |
| `*`maxDouble`*` | `xsd:double` | Limite superior do intervalo duplo. |
| `*`dateVal`*` | `xsd:dateTime` | Valor de comparação de data. |
| `*`minDate`*` | `xsd:dateTime` | Mínimo do intervalo de datas. |
| `*`maxDate`*` | `xsd:dateTime` | Máximo do intervalo de datas. |

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

