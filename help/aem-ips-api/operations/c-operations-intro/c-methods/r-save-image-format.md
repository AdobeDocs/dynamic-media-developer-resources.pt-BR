---
description: Cria um formato de imagem.
seo-description: Cria um formato de imagem.
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
topic: Dynamic Media Image Production System API
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# saveImageFormat{#saveimageformat}

Cria um formato de imagem.

>[!NOTE]
>
>O valor do campo `urlModifier` deve consistir em XML válido. Por exemplo, altere `&` para `&`. Obtenha o valor `urlModfier` da interface de usuário do IPS.

## Tipos de usuário autorizados {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Entrada (saveImageFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa com o formato de imagem com o qual você deseja trabalhar. |
| `*`imageFormatHandle`*` | `xsd:string` | Não | Identificador do formato de imagem que deseja salvar. |
| `*`name`*` | `xsd:string` | Sim | Nome do formato de imagem. |
| `*`urlModifier`*` | `xsd:string` | Sim | Pode ser qualquer cadeia de query de protocolo IPS. A maneira mais fácil de gerar um modificador de URL é criar um com a interface de usuário do IPS e, em seguida, recortar e colar a string de query. |

**Saída (saveImageFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | Sim | Lidar com o formato de imagem. |

## Exemplos {#section-c7bd733212ef494297a97093f3af193f}

Essa amostra de código cria um formato de imagem. Neste exemplo, `urlModifier` foi determinado pelo seu valor na interface do usuário do IPS com um formato HTML válido.

**Solicitação**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Resposta**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```

