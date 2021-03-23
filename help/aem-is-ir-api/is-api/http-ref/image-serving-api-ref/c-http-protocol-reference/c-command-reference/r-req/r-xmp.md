---
description: Metadados de XMP. Retorna os metadados XMP associados à imagem especificada no caminho da solicitação.
seo-description: Metadados de XMP. Retorna os metadados XMP associados à imagem especificada no caminho da solicitação.
seo-title: xmp
solution: Experience Manager
title: xmp
uuid: e1583ffe-531a-4334-b974-72df6fcb14ba
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# xmp{#xmp}

Metadados de XMP. Retorna os metadados XMP associados à imagem especificada no caminho da solicitação.

`req=xmp`

Outros comandos são ignorados. A codificação UTF-8 se aplica. A resposta é formatada como XML com tipo MIME `text/xml`.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

## Propriedades {#section-0d26b6a56c844153ae5cea4880370d00}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual.

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

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Propriedades do catálogo de imagens de consulta:

` http:// *`server`*/myRootId?req=catalogprops`

Acesse as propriedades de uma entrada do catálogo de imagens do JavaScript do lado do cliente incorporado em um arquivo HTML:

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

Recupere a imagem da máscara para uma entrada de catálogo específica, dimensionada para 25% do tamanho original:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Solicite uma imagem no tamanho de um oitavo:

` http:// *`server`*/myRootId/myImageId?scl=8`

Isso é igual a:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Solicite uma miniatura de uma imagem, dependendo dos atributos de miniatura especificados no catálogo de imagem:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Envie uma mensagem de texto para os logs do servidor:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Consulte também {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f),  [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9),  [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
