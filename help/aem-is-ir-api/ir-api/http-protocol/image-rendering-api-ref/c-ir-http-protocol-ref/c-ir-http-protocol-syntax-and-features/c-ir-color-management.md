---
description: A Renderização de imagem suporta conversões de espaço de cor com base em perfis de espaço de cor que estão em conformidade com a especificação ICC (International Color Consortium).
seo-description: A Renderização de imagem suporta conversões de espaço de cor com base em perfis de espaço de cor que estão em conformidade com a especificação ICC (International Color Consortium).
seo-title: Gerenciamento de cores da renderização da imagem *
solution: Experience Manager
title: Gerenciamento de cores da renderização da imagem *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Gerenciamento de cores da renderização da imagem *{#image-rendering-color-management}

A Renderização de imagem suporta conversões de espaço de cor com base em perfis de espaço de cor que estão em conformidade com a especificação ICC (International Color Consortium).

**Restrições**

No momento, apenas os espaços de cores CMYK, RGB e escala de cinza são suportados.

Os arquivos de estilo de gabinete (.vnc) e os arquivos de estilo de revestimento de janela ( [!DNL .vnw]) não são gerenciados por cores e presume-se que existem no espaço de cores de trabalho.

**Consulte também**

[International Color Consortium](http://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ , `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` `attribute::IccDither` , ICC Perfil Maps

## Espaços de cores padrão {#section-8ce27edf42e746febe4654f8f19b9c0c}

Cada catálogo de imagens (e o catálogo padrão) pode definir um conjunto de perfis ICC. Esses perfis constituem os espaços de cor padrão para este catálogo - uma entrada e um perfil de saída cada para dados em escala cinza, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`e `attribute::IccProfileSrcCmyk`).

O espaço de cor padrão para uma imagem específica ou outro objeto é selecionado dos perfis padrão do catálogo com base no tipo de pixel da imagem.

## Espaço de cor de entrada {#section-660f661a7e954df4b451e34134195276}

As imagens de material podem incorporar perfis ICC para definir o espaço de cor de entrada. Se nenhum perfil for incorporado em uma imagem de origem, será usado o catálogo `attribute::IccProfileSrc*` de imagens aplicável correspondente ao tipo de pixel da imagem de origem. Se esse atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` será usado. Se esse atributo do catálogo também não estiver definido, a imagem não será gerenciada por cores e apenas transformações ingênuas serão aplicadas.

## Espaço de cores de trabalho {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalmente, o espaço de cores de trabalho é definido pelo perfil de cores ICC incorporado à vinheta. Se a vinheta não incluir um perfil, o perfil de entrada RGB padrão ( `attribute::IccProfileSrcRgb` do catálogo da sessão) será usado para o espaço de cores de trabalho.

Todas as operações de renderização são executadas no espaço de cores de trabalho.

**Importante:** O perfil ICC para o espaço de cores de trabalho deve suportar transformações de entrada e saída. Se um perfil somente de saída for usado como um espaço de cor em funcionamento, o IR não conseguirá converter materiais para ele. Esse perfil de cor pode ainda ser utilizado se existirem materiais no mesmo espaço de cor de trabalho. A tentativa de aplicar materiais em outros espaços de cores falhará.

## Valores de cor explícitos {#section-31727bf1b23e477ca92572fbbf422d2f}

Pressupõe-se que os valores de cor RGB especificados com `color=`, `bgc=`, `catalog::BgColor`e `catalog::Color` existam no espaço de cores de trabalho atual.

## Arquivos de dados de material {#section-33f7a170a6664c02b8479fb89cc0aea3}

Os arquivos de imagem de material (imagens de textura e decal) podem ter o tipo de pixel RGB, escala de cinza ou CMYK e podem incorporar um perfil de cor. Se nenhum perfil de cor for incorporado, o espaço de cor de entrada padrão será associado à imagem (por exemplo, o perfil de cor do catálogo de materiais que corresponde ao tipo de pixel da imagem).

As imagens de material obtidas de solicitações aninhadas de disponibilização de imagens ou renderização de imagens normalmente incluem um perfil colorido. Se esse não for o caso, as imagens serão associadas ao espaço de cor de entrada padrão correspondente ao tipo de pixel.

Se o espaço de cores do arquivo de imagem for diferente do espaço de cores de trabalho, a conversão precisa de cores será usada para o espaço de cores de trabalho. A conversão de tipo ingênua é usada quando nenhum perfil é incorporado e nenhum perfil de entrada padrão é definido.

Outros arquivos de dados de material, como arquivos estilo gabinete ( [!DNL .vnc]) ou arquivos de revestimento de janela ( [!DNL .vnw]), não incorporam perfis coloridos e são sempre considerados como estando no espaço de cores de trabalho.

## Espaço de cor de saída {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Todas as operações de renderização ocorrem no espaço de cores de trabalho. Se a solicitação especificar um perfil de cor diferente com o `icc=` comando, os dados serão convertidos nesse espaço de cor antes de serem codificados e retornados ao cliente. Quando o gerenciamento de cores está desativado, uma conversão ingênua é usada, se necessário, para converter em escala de cinza ou CMYK.

## perfis de cores incorporados {#section-5ff733832d38429fbe02b3c1e9bb94a9}

O perfil colorido associado à imagem renderizada pode ser incorporado à imagem de resposta especificando-se `iccEmbed=` para a solicitação.

Se não `icc=` for especificado, o perfil ICC para o espaço de cores de trabalho será incorporado. Nenhum perfil é incorporado se o gerenciamento de cores estiver desativado e nenhum perfil tiver sido especificado com `icc=`.

## perfis ICC {#section-afeb76068b5042adb83261638e450140}

Todos os perfis coloridos usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC normalmente têm um sufixo [!DNL .icc] ou [!DNL .icm] arquivo e são co-localizados com arquivos de dados de material.

Embora os perfis de saída possam ser especificados pelo caminho/nome do arquivo no `icc=` comando, é recomendável registrar todos os arquivos de perfil no Mapa de Perfis ICC do catálogo padrão ou de um catálogo de material específico e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Os perfis de trabalho devem ser registrados no Mapa de Perfis ICC do catálogo de materiais ou no catálogo padrão.
