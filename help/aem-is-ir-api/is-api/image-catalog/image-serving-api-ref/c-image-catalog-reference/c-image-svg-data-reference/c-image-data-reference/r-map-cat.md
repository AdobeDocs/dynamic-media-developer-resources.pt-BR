---
description: Dados do mapa de imagem. Nenhum ou mais elementos HTML <AREA> completos, classificados de frente para trás.
solution: Experience Manager
title: Mapa
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Mapa{#map}

Dados do mapa de imagem. Nenhum ou mais elementos HTML `<AREA>` completos, classificados de frente para trás.

O servidor interpretará e poderá alterar os atributos SHAPE e COORDS. (SHAPE=CIRCLE não é suportado nesta versão.) Todos os outros atributos de `<AREA>` são passados sem modificação. Os valores de coordenadas especificados com o atributo COORDS devem ser deslocamentos de pixels do canto superior esquerdo da imagem de origem não modificada. (`%` coordenadas não são suportadas nesta versão e podem não ser processadas corretamente.)

## Propriedades {#section-f52d89fd399b4356ac05277e6c12f956}

Valor da string de texto. Se especificado, deve ser um ou mais elementos HTML `<AREA>` completos.

Esse campo participa da localização da string de texto. Consulte [Localização da cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) no *Referência do protocolo HTTP* para obter detalhes.

## Padrão {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Nenhum.

## Consulte também {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localização da sequência de caracteres de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
