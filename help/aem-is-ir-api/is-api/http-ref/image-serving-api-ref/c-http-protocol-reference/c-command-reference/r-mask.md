---
title: máscara
description: Máscara de imagem. Especifica uma imagem de máscara separada a ser usada como uma máscara não associada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# máscara{#mask}

Máscara de imagem. Especifica uma imagem de máscara separada a ser usada como uma máscara não associada.

`mask= *`objeto`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p></td> 
  <td class="stentry"> <p>Objeto de imagem a ser usado como imagem ou máscara de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Servidor de imagens aninhado, Renderização de imagens ou solicitação externa. </p></td> 
 </tr> 
</table>

*`object`* pode ser uma entrada de catálogo ou um arquivo de imagem/SVG. Pode ser especificado para camadas de imagem e camadas de cores sólidas.

Se *`object`* resolve para uma entrada de catálogo de imagens, `catalog::MaskPath` for utilizada, ou, se `catalog::MaskPath` não estiver definido, então `catalog::Path` é usada. Se *`object`* não é resolvido para uma entrada de catálogo, então é interpretado como um caminho de arquivo.

Em todos os casos, se a imagem de origem tiver um canal alfa, ela será usada. Caso contrário, a imagem é convertida em tons de cinza, se necessário, antes de ser usada como uma máscara de camada.

Se uma máscara estiver anexada a uma camada de cores sólida, ela poderá ser cortada e dimensionada usando as mesmas regras usadas para imagens em camadas de imagem. `size=`, `scale=`ou `res=` pode ser usado para dimensionar a máscara.

As máscaras de camada também podem ser especificadas no formato de um *`nestedRequest`*. As solicitações aninhadas ou incorporadas são colocadas entre chaves. Prefixe uma solicitação de Servidor de imagens incorporada com `is` e uma solicitação de renderização de imagem incorporada com `ir`. Uma solicitação para um servidor externo será presumida se nenhum prefixo for especificado. Consulte [Aninhamento e incorporação de solicitações](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) para obter detalhes.

## Propriedades {#section-a093043dc249423b8ae322cefb0d545d}

Imagem ou atributo de camada. Aplica-se à camada 0 se `layer=comp`. Ignorado pelas camadas de efeito.

*`object`* não deve resolver para um registro de catálogo que inclua um `src=` ou `mask=` comando em `catalog::Modifier`.

A variável `is` e `ir` Os prefixos não diferenciam maiúsculas de minúsculas.

## Padrão {#section-10cf793c665f49deb1b248faa3b618a9}

Se `mask=` não for especificada explicitamente e se a imagem da camada estiver associada a uma entrada de catálogo, `catalog::MaskPath` é usada. Caso contrário, o canal alfa da imagem da camada será usado, se presente. Se não houver um canal alfa, a camada não terá máscara e o retângulo será processado totalmente opaco.

## Exemplo {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Use várias máscaras separadas para colorir diferentes áreas de uma imagem. As regiões coloridas e mascaradas são colocadas em camadas sobre a imagem original não modificada:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Consulte também {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Aninhamento e incorporação de solicitações](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
