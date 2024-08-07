---
description: Cria uma imagem em camadas que pode ter várias camadas de texto e imagem.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# createTemplate{#createtemplate}

Cria uma imagem em camadas que pode ter várias camadas de texto e imagem.

O parâmetro `urlModifier` especifica os comandos de protocolo do Servidor de Imagens armazenados no catálogo do Servidor de Imagens e aplicados antes de qualquer comando fornecido pelo usuário na URL. O parâmetro `urlPostApplyModifier` especifica comandos de protocolo aplicados após qualquer comando de URL, que substitui qualquer configuração conflitante fornecida pelo usuário.

## Tipos de usuário autorizados {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Entrada (createTemplateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | A empresa à qual o modelo pertence. |
| folderHandle | `xsd:string` | Sim | O identificador de pasta que representa a pasta onde o modelo reside. |
| name | `xsd:string` | Sim | Nome do modelo. |
| type | `xsd:string` | Sim | Tipo de modelo. |
| urlModifier | `xsd:string` | Sim | Especifica os comandos do Servidor de imagens armazenados no catálogo IS que são aplicados antes de qualquer comando fornecido pelo usuário no URL. |
| urlPostApplyModifier | `xsd:string` | Não | Especifica comandos de protocolo aplicados após qualquer comando de URL, que substitui qualquer configuração conflitante fornecida pelo usuário. |

**Saída (createTemplateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetHandle | `xsd:string` | Sim | O identificador do modelo. |

## Exemplos {#section-09adb4d2f0c944af875c4463a461f55d}

Esta amostra de código cria um modelo em uma pasta especificada por um identificador, com o nome `APIcreateTemplate`, `urlModifier` e `urlPostApplyModifier`. A resposta retorna o identificador para o modelo recém-criado.

**Solicitação**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Resposta**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
