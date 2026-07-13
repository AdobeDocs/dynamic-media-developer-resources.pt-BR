---
description: Obtém valores de cadeia de caracteres das propriedades do sistema relacionadas ao Portal de Imagens.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
TQID: 'https://experienceleague.adobe.com/loaZvP3tI8neQ6ziLR-xKkkNqGGjD8Mq1jbeC8mJEQo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 0%

---

# getProperty{#getproperty}

Obtém valores de cadeia de caracteres das propriedades do sistema relacionadas ao Portal de Imagens.

As propriedades de sistema compatíveis incluem:

* `IpsVersion`: número de versão do IPS.
* `IpsImageServerUrl`: Prefixo de URL externo completo para o Servidor de Imagens IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: prefixo de URL para renderizar ativos do SVG.
* `SvgRenderEnabled`: verdadeiro se os ativos do SVG podem ser renderizados por `SvgRenderRootUrl`.

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

