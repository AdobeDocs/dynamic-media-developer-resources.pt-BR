---
description: Define vários valores de configuração específicos da empresa.
seo-description: Define vários valores de configuração específicos da empresa.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
uuid: 5908082f-6743-4444-ba73-757ad4664890
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`overwriteMode`*` | `xsd:string` | Não | Modo de substituição de ativo. |
| `*`keepPublishState`*` | `xsd:boolean` | Não | Defina como `true` para preservar o estado de publicação quando um ativo for carregado novamente. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | Não | Ativo IccProfile a ser usado como perfil de cor de origem padrão. |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | Não | Ativo IccProfile a ser usado como perfil de cor de exibição padrão. |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | Não | Ativo XSL usado para mapear metadados IPTC e EXIF para campos de metadados IPS. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | Não | Ativo XSL usado para mapear metadados XMP para campos de metadados IPS. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Não | Espaço mínimo em disco livre (em KB) disponível antes do envio de uma mensagem de aviso. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Não | Defina como `true` para enviar uma notificação aos administradores da empresa sempre que os ativos forem esvaziados da lixeira. |

**Saída (setCompanySettingsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Essa amostra de código define a configuração de uma empresa.

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
