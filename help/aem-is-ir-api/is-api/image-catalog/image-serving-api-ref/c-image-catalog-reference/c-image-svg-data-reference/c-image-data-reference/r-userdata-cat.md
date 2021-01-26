---
description: Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.
seo-description: Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.
seo-title: UserData
solution: Experience Manager
title: UserData
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# UserData{#userdata}

Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.

## Propriedades {#section-06f2002b77d54a64be07f12fff54ad13}

Valor da string de texto. É recomendável usar a formatação [dados de propriedade](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Se a formatação de dados de propriedade não for usada, a string de texto não deverá conter o caractere &#39;=&#39;.

Os clientes do visualizador de zoom, giro e folheto assumem esse campo para usar a formatação dos dados da propriedade. Esses clientes usam esse campo para configuração e personalização do visualizador. Consulte a documentação do visualizador para obter detalhes.

Esse campo participa da localização da string de texto. Consulte [Localização de cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) na *Referência de protocolo HTTP* para obter detalhes.

## Padrão {#section-7ee879762130467199745f2abc662f1e}

Nenhum.

## Consulte também {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , Localização da string de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
