---
title: res
description: Dimensionamento de imagem com base em resolução. Dimensiona a imagem para a resolução solicitada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# res{#res}

Dimensionamento de imagem com base em resolução. Dimensiona a imagem para a resolução solicitada.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Resolução de destino; normalmente em pixels por polegada (real). </p> </td> 
 </tr> 
</table>

O fator de escala é calculado pela divisão de *`val`* por `catalog::Resolution`. Observe que esse comando não afeta a resolução de impressão da imagem de resposta.

Para usar esse recurso, a resolução das imagens de origem originais deve ser conhecida e definida em `catalog::Resolution`. Dependendo do aplicativo, as unidades de resolução podem variar. Para texturas 2D repetíveis ou amostras de material, como papéis de parede ou tecidos, a resolução pode ser expressa como pixels/polegada ou pixels/mm. Fotos aéreas e mapas podem ser melhor servidos por pixels/milha ou pixels/km. Em qualquer caso, as unidades usadas para `catalog::Resolution` devem ser as mesmas unidades usadas para `res=`.

Além de obter imagens em resoluções precisas, `res=` também pode ser usado para combinar várias imagens na mesma resolução, de forma que os itens visíveis nessas imagens estejam na proporção exata entre si.

>[!NOTE]
>
>Normalmente, uma imagem composta é redimensionada para o tamanho de exibição de destino (especificado por `wid=`, `hei=` ou `attribute::DefaultPix`) antes de ser retornada ao cliente. Para evitar esse redimensionamento e obter uma imagem com a resolução exata especificada por `res=`, talvez seja necessário desabilitar o dimensionamento de exibição especificando explicitamente `scl=1`. Isso instrui o servidor a cortar a imagem composta no tamanho de exibição de destino, em vez de dimensioná-la.

## Propriedades {#section-fdbd16e59cff4952a3717146bc91412e}

Atributo de imagem/máscara do Source. Ignorado por camadas não associadas a uma imagem ou máscara de origem. Aplicado à camada 0 é especificado para `layer=comp`. Ignorado se `scale=` ou `size=` for especificado para a mesma camada.

## Padrão {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Se não especificado, `scale=` ou `size=` determina o fator de escala, ou, se nenhum dos dois for especificado, a imagem será usada sem dimensionamento.

## Exemplo {#section-eb06f333e08e4247971fb1b18922597b}

Recupere uma imagem de textura com resolução de objeto de 12 pixels/polegada para uso com Renderização de imagem ou Criação de imagem. Especificamos formato PNG sem perdas e melhor qualidade reamostragem para melhor qualidade possível,

` http:// *`servidor`*/myTexture?res=12&fmt=png&resMode=sharp`

## Consulte também {#section-1f8a8f11772e493ca803c4511f397a11}

[catálogo::Resolução](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
