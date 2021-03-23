---
description: Caminho do arquivo de máscara. Caminho relativo ou absoluto e nome de um arquivo de imagem de máscara associado a este registro de catálogo.
seo-description: Caminho do arquivo de máscara. Caminho relativo ou absoluto e nome de um arquivo de imagem de máscara associado a este registro de catálogo.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# MaskPath{#maskpath}

Caminho do arquivo de máscara. Caminho relativo ou absoluto e nome de um arquivo de imagem de máscara associado a este registro de catálogo.

Permite anexar máscaras separadas a imagens.

O servidor usa as regras de resolução de caminho descritas em [Gerenciando Dados de Origem](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) para localizar o arquivo de dados.

## Propriedades {#section-cdc3b7e2811e41008479cd97887c01b7}

Valor da string de texto. Opcional. Se especificado, deve ser um caminho de arquivo válido relativo ou absoluto do Servidor de Imagens. `attribute::DefaultExt` é anexado se nenhum sufixo de arquivo estiver presente.

Se uma imagem principal ( `catalog::Path`) e uma imagem de máscara ( `catalog::MaskPath`) forem definidas em um registro de catálogo, ambas devem ter exatamente o mesmo tamanho de pixel. As imagens da máscara devem ser em tons de cinza de 8 bits.

`mask=` nas substituições de solicitação  `catalog::MaskPath`.

`catalog::MaskPath` substitui o canal alfa na imagem principal (  `catalog::Path`), se presente, e se o canal alfa não estiver associado (ou seja, não for pré-multiplicado). Se a imagem alfa for pré-multiplicada, `catalog::MaskPath` será ignorada e o canal alfa será sempre usado.

## Padrão {#section-78533e35bfec469ba087cb68a35bb81b}

Nenhum.

## Consulte também {#section-68d262f5949c4959b8723ba44611d1dc}

[atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
