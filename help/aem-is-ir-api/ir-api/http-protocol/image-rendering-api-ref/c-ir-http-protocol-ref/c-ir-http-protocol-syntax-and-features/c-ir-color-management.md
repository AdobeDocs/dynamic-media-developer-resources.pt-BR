---
description: A Renderização de imagem suporta conversões de espaço de cores com base em perfis de espaço de cores em conformidade com a especificação ICC (International Color Consortium).
solution: Experience Manager
title: Gerenciamento de cores de renderização de imagem *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Gerenciamento de cores de renderização de imagem *{#image-rendering-color-management}

A Renderização de imagem suporta conversões de espaço de cores com base em perfis de espaço de cores em conformidade com a especificação ICC (International Color Consortium).

**Restrições**

Somente espaços de cores CMYK, RGB e tons de cinza são suportados no momento.

Arquivos de estilo de gabinete (.vnc) e arquivos de estilo de coberturas de janelas ( [!DNL .vnw]) não são gerenciados por cores e presume-se que existam no espaço de cores de trabalho.

**Consulte também**

[Consórcio internacional de cores](https://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , Mapas de perfis ICC

## Espaços de cor padrão {#section-8ce27edf42e746febe4654f8f19b9c0c}

Cada catálogo de imagens (e o catálogo padrão) pode definir um conjunto de perfis ICC. Esses perfis constituem os espaços de cores padrão para esse catálogo - um perfil de entrada e um de saída para dados em tons de cinza, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`, e `attribute::IccProfileSrcCmyk`).

O espaço de cores padrão para uma imagem específica ou outro objeto é selecionado nos perfis padrão do catálogo com base no tipo de pixel da imagem.

## Espaço de cores de entrada {#section-660f661a7e954df4b451e34134195276}

Imagens de materiais podem incorporar perfis ICC para definir o espaço de cores de entrada. Se nenhum perfil estiver incorporado em uma imagem de origem, `attribute::IccProfileSrc*` do catálogo de imagens aplicável correspondente ao tipo de pixel da imagem de origem usada. Se este atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` é usada. Se esse atributo de catálogo também não estiver definido, a imagem não será gerenciada por cores e somente transformações ingênuas serão aplicadas.

## Espaço de cor de trabalho {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalmente, o espaço de cores de trabalho é definido pelo perfil de cores ICC incorporado na vinheta. Se a vinheta não incluir um perfil, o perfil de entrada de RGB padrão ( `attribute::IccProfileSrcRgb` do catálogo de sessões) é usado para o espaço de cores de trabalho.

Todas as operações de processamento são executadas no espaço de cores de trabalho.

**Importante:** O perfil ICC para o espaço de cores de trabalho deve suportar transformações de entrada e saída. Se um perfil somente de saída for usado como um espaço de cores de trabalho, o IR não poderá converter materiais nele. Esse perfil de cores pode ainda ser utilizado se existirem materiais no mesmo espaço de cores de trabalho. A tentativa de aplicar materiais em outros espaços de cores falhará.

## Valores de cor explícitos {#section-31727bf1b23e477ca92572fbbf422d2f}

valores de cor de RGB especificados com `color=`, `bgc=`, `catalog::BgColor`, e `catalog::Color` presume-se que existam no espaço de cores de trabalho atual.

## Arquivos de dados de material {#section-33f7a170a6664c02b8479fb89cc0aea3}

Os arquivos de imagem de material (imagens de textura e de decalque) podem ter o tipo de pixel RGB, tons de cinza ou CMYK e podem incorporar um perfil de cores. Se nenhum perfil de cores estiver incorporado, o espaço de cores de entrada padrão será associado à imagem (por exemplo, o perfil de cores do catálogo de materiais que corresponde ao tipo de pixel da imagem).

Imagens de materiais obtidas de solicitações aninhadas de Disponibilização de imagens ou Renderização de imagens normalmente incluem um perfil de cores. Se esse não for o caso, as imagens serão associadas ao espaço de cor de entrada padrão correspondente ao tipo de pixel.

Se o espaço de cores do arquivo de imagem for diferente do espaço de cores de trabalho, a conversão precisa de cores será usada para converter para o espaço de cores de trabalho. A conversão de tipo naïve é usada quando nenhum perfil é incorporado e nenhum perfil de entrada padrão é definido.

Outros arquivos de dados de material, como arquivos de estilo de gabinete ( [!DNL .vnc]) ou arquivos de cobertura de janelas ( [!DNL .vnw]) não incorporam perfis de cores e sempre se presume que estão no espaço de cores de trabalho.

## Espaço de cor de saída {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Todas as operações de desenho ocorrem no espaço de cores de trabalho. Se a solicitação especificar um perfil de cor diferente com o `icc=` os dados são convertidos para esse espaço de cores antes de serem codificados e retornados ao cliente. Quando o gerenciamento de cores está desativado, a conversão ingênua é usada, se necessário, para converter em tons de cinza ou CMYK.

## Perfis de cores incorporados {#section-5ff733832d38429fbe02b3c1e9bb94a9}

O perfil de cores associado à imagem renderizada pode ser incorporado à imagem de resposta especificando `iccEmbed=` para a solicitação.

Se `icc=` não for especificado, o perfil ICC do espaço de cores de trabalho será incorporado. Nenhum perfil será incorporado se o gerenciamento de cores estiver desativado e nenhum perfil tiver sido especificado com `icc=`.

## Perfis ICC {#section-afeb76068b5042adb83261638e450140}

Todos os perfis de cores usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC normalmente têm um [!DNL .icc] ou [!DNL .icm] sufixo de arquivo e estão co-localizados com arquivos de dados de material.

Embora os perfis de saída possam ser especificados por caminho/nome de arquivo no `icc=` , é recomendável registrar todos os arquivos de perfil no Mapa de perfil ICC do catálogo padrão ou em um catálogo de materiais específico e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Os perfis de trabalho devem ser registrados no Mapa de perfil ICC do catálogo de materiais ou no catálogo padrão.
