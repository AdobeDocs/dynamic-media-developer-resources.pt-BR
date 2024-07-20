---
description: Cria um formato de imagem.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# saveImageFormat{#saveimageformat}

Cria um formato de imagem.

>[!NOTE]
>
>O valor do campo `urlModifier` deve consistir em XML válido. Por exemplo, altere `&` para `&`. Obter o valor `urlModfier` da interface de usuário do IPS.

## Tipos de usuário autorizados {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Entrada (saveImageFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com o formato de imagem que você deseja trabalhar. |
| imageFormatHandle | `xsd:string` | Não | O identificador de formato de imagem que você deseja salvar. |
| name | `xsd:string` | Sim | Nome do formato de imagem. |
| urlModifier | `xsd:string` | Sim | Pode ser qualquer sequência de consulta de protocolo IPS. A maneira mais fácil de gerar um modificador de URL é criar um com a interface de usuário IPS e, em seguida, recortar e colar a sequência de consulta. |

**Saída (saveImageFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Sim | Processe o formato da imagem. |

## Exemplos {#section-c7bd733212ef494297a97093f3af193f}

Essa amostra de código cria um formato de imagem. Neste exemplo, `urlModifier` foi determinado pelo seu valor na interface de usuário do IPS com um formato de HTML válido.

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
