---
description: Dados do usuário. O servidor retorna o conteúdo desse campo para o cliente em resposta a req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: 'https://experienceleague.adobe.com/9jhCw--mmCQ1-j1uNGFmfTEcnkNzxbKfXJtve5GugdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
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
