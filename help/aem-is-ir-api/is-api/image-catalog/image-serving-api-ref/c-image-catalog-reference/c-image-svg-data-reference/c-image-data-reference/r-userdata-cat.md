---
description: Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# UserData{#userdata}

Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.

## Propriedades {#section-06f2002b77d54a64be07f12fff54ad13}

Valor da string de texto. É recomendável usar a formatação de [dados de propriedade](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Se a formatação de dados de propriedade não for usada, a cadeia de texto não deverá conter o caractere &#39;=&#39;.

Os clientes do visualizador de zoom, rotação e folheto assumem que esse campo usa a formatação de dados de propriedade. Esses clientes usam esse campo para configuração e personalização do visualizador. Consulte a documentação do visualizador para obter detalhes.

Este campo participa da localização da sequência de caracteres de texto. Consulte [Localização de Cadeia de Caracteres de Texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) na *Referência de Protocolo HTTP* para obter detalhes.

## Padrão {#section-7ee879762130467199745f2abc662f1e}

Nenhum.

## Consulte também {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localização da Cadeia de Caracteres de Texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
