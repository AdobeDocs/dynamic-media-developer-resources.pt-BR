---
description: Caminho raiz dos dados de origem. Valor da string de texto. Caminho absoluto ou segmento de caminho relativo para a pasta raiz de todos os arquivos de dados de vinheta, textura, imagem e ICC referenciados por este catálogo de imagem.
seo-description: Caminho raiz dos dados de origem. Valor da string de texto. Caminho absoluto ou segmento de caminho relativo para a pasta raiz de todos os arquivos de dados de vinheta, textura, imagem e ICC referenciados por este catálogo de imagem.
seo-title: RootPath *
solution: Experience Manager
title: RootPath *
uuid: a23ea524-8ca4-47c4-83a5-64a174d8767e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# RootPath *{#rootpath}

Caminho raiz dos dados de origem. Valor da string de texto. Caminho absoluto ou segmento de caminho relativo para a pasta raiz de todos os arquivos de dados de vinheta, textura, imagem e ICC referenciados por este catálogo de imagem.

## Propriedades {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Sequência de texto. Deve estar vazio, um segmento de caminho válido relativo à configuração do servidor de Renderização de Imagem `ir.resourceRootPaths` ou um caminho de arquivo absoluto válido. Não deve incluir delimitadores de elemento de caminho à esquerda e à direita.

## Padrão {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Herdado de `default::RootPath` se não estiver definido. Se definido, mas vazio, não contribuirá para o caminho raiz do arquivo de origem.

## Consulte também {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
