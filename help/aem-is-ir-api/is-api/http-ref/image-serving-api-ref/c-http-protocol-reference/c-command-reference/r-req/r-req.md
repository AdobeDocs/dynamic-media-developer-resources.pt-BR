---
description: Tipo de solicitação. Especifica o tipo de solicitação.
seo-description: Tipo de solicitação. Especifica o tipo de solicitação.
seo-title: req
solution: Experience Manager
title: req
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# req{#req}

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
* [mrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [resolve](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [targets](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validate](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Salvo indicação em contrário nas descrições detalhadas, o servidor retornará `text` respostas com o tipo MIME `text/plain`. Muitos tipos de solicitação permitem especificar um tipo de resposta, como `text`, que normalmente é o padrão, `javascript`, `xml` ou `json`. Os tipos MIME de resposta associados são `text/plain`, `text/javascript`, `text/xml` e `text/javascript`, respectivamente.

Salvo indicação em contrário, as respostas formatar a resposta como um conjunto de pares `name=value`.

Consulte [Propriedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
