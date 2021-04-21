---
description: Obtém valores de sequência de caracteres das propriedades do sistema relacionadas ao Portal de Imagem.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# getProperty{#getproperty}

Obtém valores de sequência de caracteres das propriedades do sistema relacionadas ao Portal de Imagem.

As propriedades do sistema compatíveis incluem:

* `IpsVersion`: Número de versão do IPS.
* `IpsImageServerUrl`: Prefixo completo e externo de URL para o Servidor de Imagem do IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: Prefixo de URL para renderizar ativos SVG.
* `SvgRenderEnabled`: True se os ativos SVG puderem ser renderizados por  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Tamanho máximo (em bytes) de dados de arquivo permitidos em um upload  [!DNL POST]. O sistema rejeita arquivos maiores que o limite máximo.

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
| `*`name`*` | `xsd:string` | Sim | O nome da propriedade a ser obtida. |

**Saída (getPropertyReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`value`*` | `xsd:string` | Sim | O valor da propriedade. |

## Exemplos {#section-3f80a78dd60c404181b34d3a912d7a36}

Essa amostra de código usa uma constante de string Propriedades do IPS para retornar um valor específico. Neste exemplo, a propriedade IPS é a versão do servidor IPS.

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

