---
title: RootPath
description: Caminho raiz de dados do Source. Valor da string de texto. Caminho absoluto ou segmento de caminho relativo para a pasta raiz de todos os arquivos de dados de vinheta, textura, imagem e ICC referenciados por este catálogo de imagens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# RootPath{#rootpath}

Caminho raiz de dados do Source. Valor da string de texto. Caminho absoluto ou segmento de caminho relativo para a pasta raiz de todos os arquivos de dados de vinheta, textura, imagem e ICC referenciados por este catálogo de imagens.

## Propriedades {#section-5ff1cf592dd24dfc8cfa470c753ab828}

String de texto. Deve ser um segmento de caminho válido relativo à configuração `ir.resourceRootPaths` do servidor de Renderização de Imagem ou um caminho de arquivo absoluto válido. Não deve incluir delimitadores de elementos de caminho à esquerda e à direita.

## Padrão {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Herdado de `default::RootPath` se não estiver definido. Se definido, mas vazio, não contribui para o caminho raiz do arquivo de origem.

## Consulte também {#section-92012cc1ce32448ea977e7e0484857e2}

[catálogo::Caminho](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catálogo::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`

