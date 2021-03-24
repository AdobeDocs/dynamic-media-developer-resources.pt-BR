---
description: Coordenadas de localização da imagem retornadas pela operação getPhotoshopPath.
solution: Experience Manager
title: PerspectivaQuad
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# PerspectivaQuad{#perspectivequad}

Coordenadas de localização da imagem retornadas pela operação getPhotoshopPath.

Sintaxe

## Parâmetros {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`x0`*` | `xsd:double` | Coordenada superior esquerda do eixo x. |
| `*`y0`*` | `xsd:double` | Coordenada do eixo y superior esquerda. |
| `*`x1`*` | `xsd:double` | Coordenada do eixo x superior direito. |
| `*`y1`*` | `xsd:double` | Coordenada do eixo y superior direito. |
| `*`x2`*` | `xsd:double` | Coordenada do eixo x inferior direito. |
| `*`y2`*` | `xsd:double` | Coordenada do eixo y inferior direito. |
| `*`x3`*` | `xsd:double` | Correspondência do eixo x esquerdo inferior. |
| `*`y3`*` | `xsd:double` | Coordenada inferior do eixo y à esquerda. |

## Exemplo {#section-19ed4409ff3a41c9b52a9c9424612927}

O tipo `PerspectiveQuad` retorna dados nesta ordem:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

