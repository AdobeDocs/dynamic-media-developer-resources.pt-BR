---
description: Nitidez da imagem. Aplica um filtro básico de nitidez à camada ou à imagem de visualização final, depois de todo o dimensionamento, se layer=comp.
seo-description: Nitidez da imagem. Aplica um filtro básico de nitidez à camada ou à imagem de visualização final, depois de todo o dimensionamento, se layer=comp.
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sharpen{#op-sharpen}

Nitidez da imagem. Aplica um filtro básico de nitidez à camada ou à imagem de visualização final, depois de todo o dimensionamento, se layer=comp.

`op_sharpen=0|1`

A máscara de camada ou a máscara composta também são afiadas.

## Propriedades {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Atributo de camada ou atributo de visualização. Aplica-se à camada atual ou à imagem de visualização final, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, para nenhum efeito de nitidez.

## Example {#section-3202122df5db4e14b358ecabfb6d8b85}

Compense o leve desfoque causado pela reamostragem da imagem. Também aumentamos a qualidade do JPEG para evitar artefatos JPEG adicionais ao longo das bordas afiadas.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Consulte também {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
