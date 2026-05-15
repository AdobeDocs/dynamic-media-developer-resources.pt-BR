---
description: Identificador de registro do catálogo
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# ID {#id}

Valor da chave de índice pelo qual os registros no arquivo de dados de imagem são pesquisados por [!DNL Platform Server].

Normalmente, um identificador de imagem curto e exclusivo, como um número SKU, possivelmente com algum tipo de sufixo de imagem, se um SKU tiver várias imagens. Também pode ser uma sequência de caracteres mais complexa que se parece mais com um caminho de arquivo, para suportar o redirecionamento fácil de sites com o Servidor de imagens.

## Propriedades {#id-properties}

String de texto. Obrigatório. Chave de índice principal da tabela de dados de imagem. Cada valor catalog::Id deve ser exclusivo na tabela.

## Padrão {#id-default}

Nenhum.

## Consulte também {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
