---
description: Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# UserData{#userdata}

Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.

## Propriedades {#section-06f2002b77d54a64be07f12fff54ad13}

Valor da string de texto. É recomendável usar a formatação [property data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Se a formatação de dados de propriedade não for usada, a cadeia de caracteres de texto não deverá conter o caractere &#39;=&#39;.

Os clientes do visualizador de zoom, rotação e folheto assumem esse campo para usar a formatação de dados de propriedade. Esses clientes usam esse campo para configuração e personalização do visualizador. Consulte a documentação do visualizador para obter detalhes.

Esse campo participa da localização da string de texto. Consulte [Localização da cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) no *Referência do protocolo HTTP* para obter detalhes.

## Padrão {#section-7ee879762130467199745f2abc662f1e}

Nenhum.

## Consulte também {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , Localização da sequência de caracteres de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
