---
description: Caminho do arquivo de máscara. Caminho e nome relativos ou absolutos de um arquivo de imagem de máscara associado a este registro de catálogo.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# MaskPath{#maskpath}

Caminho do arquivo de máscara. Caminho e nome relativos ou absolutos de um arquivo de imagem de máscara associado a este registro de catálogo.

Permite anexar máscaras separadas a imagens.

O servidor usa as regras de resolução de caminho descritas em [Gerenciando Dados do Source](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) para localizar o arquivo de dados.

## Propriedades {#section-cdc3b7e2811e41008479cd97887c01b7}

Valor da string de texto. Opcional. Se especificado, deve ser um caminho de arquivo relativo ou absoluto do Servidor de imagens. `attribute::DefaultExt` será acrescentado se nenhum sufixo de arquivo estiver presente.

Se uma imagem principal ( `catalog::Path`) e uma imagem de máscara ( `catalog::MaskPath`) forem definidas em um registro de catálogo, ambas deverão ter exatamente o mesmo tamanho de pixel. As imagens de máscara devem ser em tons de cinza de 8 bits.

`mask=` na solicitação substitui `catalog::MaskPath`.

`catalog::MaskPath` substitui o canal alfa na imagem principal ( `catalog::Path`), se presente, e se o canal alfa não está associado (isto é, não é pré-multiplicado). Se a imagem alfa for pré-multiplicada, `catalog::MaskPath` será ignorado e o canal alfa sempre será usado.

## Padrão {#section-78533e35bfec469ba087cb68a35bb81b}

Nenhum.

## Consulte também {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
