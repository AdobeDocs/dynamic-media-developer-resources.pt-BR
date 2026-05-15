---
description: Define vários valores de configuração específicos da empresa.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: 'https://experienceleague.adobe.com/df-NUZDApA-q0a-A3oxM6PUQUoVmGy8gqS4HU8lhfvc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 0%

---

# setCompanySettings{#setcompanysettings}

Define vários valores de configuração específicos da empresa.

Sintaxe

## Tipos de usuário autorizados {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-a472da6c57c74a94a179dda081004888}

**Entrada (setCompanySettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| overwriteMode | `xsd:string` | Não | Modo de substituição de ativo. |
| keepPublishState | `xsd:boolean` | Não | Defina como `true` para preservar o estado de publicação quando um ativo for recarregado. |
| defaultSourceProfileHandle | `xsd:string` | Não | Ativo IccProfile a ser usado como perfil de cor de origem padrão. |
| defaultDisplayProfileHandle | `xsd:string` | Não | Ativo IccProfile a ser usado como perfil de cor de exibição padrão. |
| iptcExifMappingXsltHandle | `xsd:string` | Não | Ativo XSL usado para mapear metadados IPTC e EXIF para campos de metadados IPS. |
| xmpMappingXsltHandle | `xsd:string` | Não | Ativo XSL usado para mapear metadados do XMP para campos de metadados IPS. |
| diskSpaceWarningMin | `xsd:int` | Não | Mínimo de espaço livre em disco (em KB) disponível antes do envio de uma mensagem de aviso. |
| emailTrashCleanupWarning | `xsd:boolean` | Não | Defina como `true` para enviar uma notificação aos administradores da empresa sempre que os ativos forem esvaziados da lixeira. |

**Saída (setCompanySettingsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Esta amostra de código define a configuração de uma empresa.

**Solicitação**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Resposta**

Nenhum.
