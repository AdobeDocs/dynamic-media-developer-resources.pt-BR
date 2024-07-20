---
description: Coordenadas do local da imagem retornadas pela operação getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Coordenadas do local da imagem retornadas pela operação getPhotoshopPath.

Sintaxe

## Parâmetros {#section-59792c446366456d90de7f5875bad1b0}

| Nome | Tipo | Descrição |
|---|---|---|
| x0 | `xsd:double` | Coordenada superior esquerda do eixo x. |
| y0 | `xsd:double` | Coordenada superior esquerda do eixo Y. |
| x1 | `xsd:double` | Coordenada superior direita do eixo x. |
| y1 | `xsd:double` | Coordenada superior direita do eixo Y. |
| x2 | `xsd:double` | Coordenada inferior direita do eixo x. |
| y2 | `xsd:double` | Coordenada inferior direita do eixo Y. |
| x3 | `xsd:double` | Coordenada inferior esquerda do eixo x. |
| y3 | `xsd:double` | Coordenada inferior esquerda do eixo Y. |

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
