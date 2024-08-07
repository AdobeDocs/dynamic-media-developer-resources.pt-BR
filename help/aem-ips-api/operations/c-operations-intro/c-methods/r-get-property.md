---
description: Obtém valores de cadeia de caracteres das propriedades do sistema relacionadas ao Portal de Imagens.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# getProperty{#getproperty}

Obtém valores de cadeia de caracteres das propriedades do sistema relacionadas ao Portal de Imagens.

As propriedades de sistema compatíveis incluem:

* `IpsVersion`: número de versão do IPS.
* `IpsImageServerUrl`: Prefixo de URL externo completo para o Servidor de Imagens IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: prefixo de URL para renderizar ativos SVG.
* `SvgRenderEnabled`: verdadeiro se os ativos de SVG puderem ser renderizados por `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Tamanho máximo (em bytes) de dados de arquivo permitido em um carregamento [!DNL POST]. O sistema rejeita arquivos maiores que o limite máximo.

## Tipos de usuário autorizados {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Entrada (getPropertyParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| name | `xsd:string` | Sim | O nome da propriedade a ser obtida. |

**Saída (getPropertyReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| value | `xsd:string` | Sim | O valor da propriedade. |

## Exemplos {#section-3f80a78dd60c404181b34d3a912d7a36}

Esta amostra de código usa uma constante de string de Propriedades de IPS para retornar um valor específico. Neste exemplo, a propriedade IPS é a versão do servidor IPS.

**Solicitação**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Resposta**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
