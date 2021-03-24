---
description: Máscara de imagem. Especifica uma imagem de máscara separada a ser usada como uma máscara não associada.
solution: Experience Manager
title: máscara
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---


# máscara{#mask}

Máscara de imagem. Especifica uma imagem de máscara separada a ser usada como uma máscara não associada.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p></td> 
  <td class="stentry"> <p>Objeto de imagem a ser usado como imagem ou máscara de camada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> anestedRequest</span> </p></td> 
  <td class="stentry"> <p>Serviço de imagem aninhado, Renderização de imagem ou solicitação externa. </p></td> 
 </tr> 
</table>

*`object`* pode ser uma entrada de catálogo ou um arquivo image/SVG. Pode ser especificado para camadas de imagem e camadas de cor sólida.

Se *`object`* for resolvido para uma entrada de catálogo de imagem, `catalog::MaskPath` será usado ou, se `catalog::MaskPath` não for definido, `catalog::Path` será usado. Se *`object`* não for resolvido para uma entrada de catálogo, então ele será interpretado como um caminho de arquivo.

Em todos os casos, se a imagem de origem tiver um canal alfa, ela será usada. Caso contrário, a imagem será convertida em tons de cinza, se necessário, antes de usá-la como uma máscara de camada.

Se uma máscara for anexada a uma camada de cor sólida, ela poderá ser cortada e dimensionada usando as mesmas regras usadas para imagens em camadas de imagem. `size=`,  `scale=` ou  `res=` pode ser usada para dimensionar a máscara.

Máscaras de camada também podem ser especificadas na forma de um *`nestedRequest`*. As solicitações aninhadas ou incorporadas são fechadas por chaves. Coloque o prefixo `is` em uma solicitação incorporada de Exibição de imagem com `ir`. Uma solicitação para um servidor externo é assumida se nenhum prefixo for especificado. Consulte [Solicitar aninhamento e incorporação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) para obter detalhes.

## Propriedades {#section-a093043dc249423b8ae322cefb0d545d}

Imagem ou atributo de camada. Aplica-se à camada 0 se `layer=comp`. Ignorado por camadas de efeito.

*`object`* não deve ser resolvido para um registro de catálogo que inclua um  `src=` comando  `mask=` ou no  `catalog::Modifier`.

Os prefixos `is` e `ir` não diferenciam maiúsculas de minúsculas.

## Padrão {#section-10cf793c665f49deb1b248faa3b618a9}

Se `mask=` não for especificado explicitamente e se a imagem da camada estiver associada a uma entrada de catálogo, então `catalog::MaskPath` será usado. Caso contrário, o canal alfa da imagem da camada será usado, se presente. Se não houver um canal alfa, a camada não terá máscara e o retângulo da camada será renderizado completamente opaco.

## Exemplo {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Use várias máscaras separadas para colorir diferentes áreas de uma imagem. As regiões coloridas e mascaradas são colocadas em camadas sobre a imagem original e não modificada:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Consulte também {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Nested and Embeading](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
