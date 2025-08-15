---
description: Metadados do XMP. Retorna os metadados do XMP associados à imagem especificada no caminho da solicitação.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# xmp{#xmp}

Metadados do XMP. Retorna os metadados do XMP associados à imagem especificada no caminho da solicitação.

`req=xmp`

Outros comandos são ignorados. A codificação UTF-8 se aplica. A resposta está formatada como XML com o tipo MIME `text/xml`.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.

## Propriedades {#section-0d26b6a56c844153ae5cea4880370d00}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada.

## Padrão {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Se o URL não incluir um caminho de imagem ou modificadores, então:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Caso contrário, `req=img`

## Exemplos {#section-34213692deab4a0f9037d5844132ee14}

Propriedades do arquivo de imagem de consulta.

` http:// *`servidor`*/myPath/myImage.tif?req=imageprops`

Propriedades do catálogo de imagens de consulta:

` http:// *`servidor`*/myRootId?req=catalogprops`

Acesse as propriedades de uma entrada de catálogo de imagem do JavaScript do lado do cliente incorporado em um arquivo HTML:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Recupere a imagem da máscara de uma entrada de catálogo específica, dimensionada para 25% do tamanho original:

` http:// *`servidor`*/myRootId/myImageId?req=mask&scale=0.25`

Solicitar uma imagem no tamanho de um oitavo:

` http:// *`servidor`*/myRootId/myImageId?scl=8`

É o mesmo que:

` http:// *`servidor`*/myRootId/myImageId?req=img&scl=8`

Solicite uma miniatura de uma imagem, dependendo dos atributos de miniatura especificados no catálogo de imagens:

` http:// *`servidor`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Enviar uma mensagem de texto para os logs do servidor:

` http:// *`servidor`*/myRootId?req=message&message=This%20is%20the%20message`

## Consulte também {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [catálogo::Destinos](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catálogo::Dados do Usuário](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), [Escala de Miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f), [Propriedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), [Mapas de Imagens](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
