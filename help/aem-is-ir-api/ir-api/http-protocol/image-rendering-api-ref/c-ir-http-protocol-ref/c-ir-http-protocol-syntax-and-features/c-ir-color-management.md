---
description: A Renderização de imagem suporta conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).
seo-description: A Renderização de imagem suporta conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).
seo-title: Gestão de cores da renderização de imagens *
solution: Experience Manager
title: Gestão de cores da renderização de imagens *
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---


# Gestão de cores da renderização de imagens *{#image-rendering-color-management}

A Renderização de imagem suporta conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).

**Restrições**

Somente os espaços de cores CMYK, RGB e em escala de cinza são suportados no momento.

Arquivos de estilo de gabinete (.vnc) e arquivos de estilo de cobertura de janela ( [!DNL .vnw]) não são gerenciados por cores e presumem-se existir no espaço de cores de trabalho.

**Consulte também**

[Mapas de perfil do International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` ,  `attribute::IccDither` , ICC

## Espaços de cores padrão {#section-8ce27edf42e746febe4654f8f19b9c0c}

Cada catálogo de imagem (e o catálogo padrão) pode definir um conjunto de perfis ICC. Esses perfis constituem os espaços de cores padrão para esse catálogo - uma entrada e um perfil de saída cada para dados em escala de cinza, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` e `attribute::IccProfileSrcCmyk`).

O espaço de cores padrão para uma imagem específica ou outro objeto é selecionado nos perfis padrão do catálogo com base no tipo de pixel da imagem.

## Espaço de cores de entrada {#section-660f661a7e954df4b451e34134195276}

Imagens de material podem incorporar perfis ICC para definir o espaço de cores de entrada. Se nenhum perfil for incorporado em uma imagem de origem, `attribute::IccProfileSrc*` do catálogo de imagem aplicável correspondente ao tipo de pixel da imagem de origem será usado. Se este atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` será usado. Se esse atributo de catálogo também não estiver definido, a imagem não será gerenciada por cores e apenas transformações ingênuas serão aplicadas.

## Espaço de cores de trabalho {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalmente, o espaço de cores de trabalho é definido pelo perfil de cores ICC incorporado na vinheta. Se a vinheta não incluir um perfil, o perfil de entrada RGB padrão ( `attribute::IccProfileSrcRgb` do catálogo de sessão) será usado para o espaço de cores de trabalho.

Todas as operações de renderização são executadas no espaço de cores de trabalho.

**Importante:** o perfil ICC do espaço de cores de trabalho deve suportar transformações de entrada e saída. Se um perfil somente de saída for usado como um IR do espaço de cores em funcionamento, não será possível converter materiais nele. Esse perfil de cor pode ainda ser utilizado se existirem materiais no mesmo espaço de cores de trabalho. A tentativa de aplicar materiais em outros espaços de cores falhará.

## Valores de cor explícitos {#section-31727bf1b23e477ca92572fbbf422d2f}

Pressupõe-se que os valores de cores RGB especificados com `color=`, `bgc=`, `catalog::BgColor` e `catalog::Color` existam no espaço de cores de trabalho atual.

## Arquivos de dados de material {#section-33f7a170a6664c02b8479fb89cc0aea3}

Os arquivos de imagem de material (imagens de textura e decalque) podem ter o tipo de pixel RGB, escala de cinza ou CMYK e podem incorporar um perfil de cor. Se nenhum perfil de cor for incorporado, o espaço de cores de entrada padrão será associado à imagem (por exemplo, o perfil de cores do catálogo de materiais que corresponde ao tipo de pixel da imagem).

Imagens de material obtidas de solicitações aninhadas de Exibição de imagem ou Renderização de imagem normalmente incluem um perfil de cor. Se esse não for o caso, as imagens serão associadas ao espaço de cores de entrada padrão correspondente ao tipo de pixel.

Se o espaço de cores do arquivo de imagem for diferente do espaço de cores de trabalho, a conversão precisa de cores será usada para converter para o espaço de cores de trabalho. A conversão de tipo ingênuo é usada quando nenhum perfil é incorporado e nenhum perfil de entrada padrão é definido.

Outros arquivos de dados de material, como arquivos de estilo de gabinete ( [!DNL .vnc]) ou arquivos de cobertura de janela ( [!DNL .vnw]), não incorporam perfis de cores e são sempre considerados como estando no espaço de cores de trabalho.

## Espaço de cores de saída {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Todas as operações de renderização ocorrem no espaço de cores de trabalho. Se a solicitação especificar um perfil de cor diferente com o comando `icc=`, os dados serão convertidos para esse espaço de cor antes de serem codificados e retornados ao cliente. Quando o gerenciamento de cores está desativado, a conversão ingênua é usada, se necessário, para conversão em escala de cinza ou CMYK.

## Perfis de cores incorporados {#section-5ff733832d38429fbe02b3c1e9bb94a9}

O perfil de cor associado à imagem renderizada pode ser incorporado à imagem de resposta especificando `iccEmbed=` para a solicitação.

Se `icc=` não for especificado, o perfil ICC para o espaço de cores de trabalho será incorporado. Nenhum perfil será incorporado se o gerenciamento de cores estiver desativado e nenhum perfil tiver sido especificado com `icc=`.

## Perfis ICC {#section-afeb76068b5042adb83261638e450140}

Todos os perfis de cores usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC geralmente têm um sufixo de arquivo [!DNL .icc] ou [!DNL .icm] e são co-localizados com arquivos de dados de material.

Embora os perfis de saída possam ser especificados por caminho/nome de arquivo no comando `icc=`, é recomendável registrar todos os arquivos de perfil no Mapa de perfil ICC do catálogo padrão ou de um catálogo de material específico e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Os perfis de trabalho devem ser registrados no Mapa de Perfil ICC do catálogo de materiais ou no catálogo padrão.
