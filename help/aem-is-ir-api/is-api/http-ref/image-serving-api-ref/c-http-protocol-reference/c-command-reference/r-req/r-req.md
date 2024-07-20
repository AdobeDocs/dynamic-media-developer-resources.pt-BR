---
description: Tipo de solicitação. Especifica o tipo de solicitação.
solution: Experience Manager
title: solic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# solic{#req}

Tipo de solicitação. Especifica o tipo de solicitação.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`opções`*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [mapa](r-map-req.md)
* [máscara](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [mensagem](r-message.md)
* [props](r-props.md)
* [resolver](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [targets](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validar](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

A menos que seja observado de outra forma nas descrições detalhadas, o servidor retorna `text` respostas com o tipo MIME `text/plain`. Muitos tipos de solicitações permitem que você especifique um tipo de resposta, como `text`, que normalmente é o padrão, `javascript`, `xml` ou `json`. Os tipos MIME de resposta associados são `text/plain`, `text/javascript`, `text/xml` e `text/javascript`, respectivamente.

A menos que seja observado o contrário, as respostas formatam a resposta como um conjunto de pares `name=value`.

Consulte [Propriedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
