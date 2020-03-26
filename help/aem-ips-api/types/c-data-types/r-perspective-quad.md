---
description: Coordenadas de localização da imagem retornadas pela operação getPhotoshopPath.
seo-description: Coordenadas de localização da imagem retornadas pela operação getPhotoshopPath.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
topic: Scene7 Image Production System API
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# PerspectiveQuad{#perspectivequad}

Coordenadas de localização da imagem retornadas pela operação getPhotoshopPath.

Sintaxe

## Parâmetros {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`x0`*` | `xsd:double` | Coordenada superior esquerda do eixo x. |
| ` *`y0`*` | `xsd:double` | Coordenada superior do eixo y à esquerda. |
| ` *`x1`*` | `xsd:double` | Coordenada do eixo x superior direito. |
| ` *`y1`*` | `xsd:double` | Coordenada do eixo y superior direito. |
| ` *`x2`*` | `xsd:double` | Coordenada do eixo x inferior direito. |
| ` *`y2`*` | `xsd:double` | Coordenada do eixo y inferior direito. |
| ` *`x3`*` | `xsd:double` | Coordenação do eixo x esquerdo inferior. |
| ` *`y3`*` | `xsd:double` | Coordenada inferior do eixo y à esquerda. |

## Example {#section-19ed4409ff3a41c9b52a9c9424612927}

O `PerspectiveQuad` tipo retorna dados nesta ordem:

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

