---
title: Gerenciamento de cores do Servidor de imagens
description: O Servidor de imagens suporta conversões de espaço de cores com base em perfis de espaço de cores em conformidade com a especificação ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# Gerenciamento de cores do Servidor de imagens{#image-serving-color-management}

O Servidor de imagens suporta conversões de espaço de cores com base em perfis de espaço de cores em conformidade com a especificação ICC (International Color Consortium).

## Espaços de cor padrão {#section-8cfe60808bce49968091995e4e521dba}

Cada catálogo de imagens (e o catálogo padrão) pode definir um conjunto de perfis ICC que constituem os espaços de cores padrão para esse catálogo - uma entrada e um perfil de saída para cada um dos dados em tons de cinza, RGB e CMYK. Consulte
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[atributo::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Espaço de cores de entrada {#section-9f08e2c1b6aa4fe4815be174972c1944}

As imagens do Source podem incorporar perfis ICC para definir o espaço de cores de entrada. Se nenhum perfil estiver incorporado em uma imagem de origem, `attribute::IccProfileSrc*` do catálogo de imagens aplicável correspondente ao tipo de pixel da imagem de origem será usado. Se este atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` será usado. Se esse atributo de catálogo também não estiver definido, a imagem não será gerenciada por cores e somente transformações ingênuas serão aplicadas.

## Espaço de cor de saída {#section-b517bca622b64dcfa7defba6035d0716}

O espaço de cores do resultado final da imagem de uma solicitação é definido com o comando `icc=`. Se `icc=` não for especificado, o espaço de cores de saída padrão (do catálogo principal da solicitação) que corresponde ao tipo de pixel da imagem de saída será usado como o espaço de cores de saída. Se nenhum perfil de saída for definido no catálogo principal ou padrão, e se a camada base for uma imagem com um perfil incorporado correspondente ao tipo de pixel de saída, esse perfil será usado para o espaço de cores de saída. Caso contrário, o espaço de cores de saída permanece indefinido — somente conversões de cores ingênuas são aplicadas ao converter entre tipos de pixel e nenhum perfil de cor pode ser incorporado na imagem de saída.

O espaço de cores de saída de uma solicitação do Servidor de imagens aninhada/incorporada é sempre o mesmo que o espaço de cores de saída da solicitação externa de incorporação.

## Cores sólidas {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Os valores de cor especificados com `color=`, `bgcolor=` ou o comando RTF `\iscolortbl` são associados ao espaço de cor de entrada se o valor de cor incluir o sufixo &#39;S&#39;, caso contrário, eles serão associados ao espaço de cor de saída. Os valores de cor especificados com `bgc=` ou os comandos RTF `\colortbl` e `\cmykcolortbl` são sempre associados ao espaço de cor de saída padrão ou real correspondente.

>[!NOTE]
>
>No momento, `bgc=` não participa totalmente do gerenciamento de cores - o sufixo &#39;S&#39; é ignorado quando especificado com `bgc=`, e a conversão naïve é aplicada quando o tipo de pixel do valor de cor especificado com `bgc=` difere do tipo de pixel da imagem de saída. Caso contrário, `bgc=` será associado ao espaço de cores de saída real.

## Solicitações aninhadas e incorporadas {#section-bdda638c31504f26a77e51ebb1ea6e3b}

O espaço de cores de saída para solicitações IS aninhadas e solicitações IR inseridas é automaticamente definido para o espaço de cores de saída da solicitação mais externa, a menos que a solicitação aninhada especifique um espaço de cores de saída explícito com `icc=`. Além disso, as solicitações aninhadas/incorporadas também herdam os espaços de cores de saída padrão do catálogo principal da solicitação mais externa, para garantir o tratamento consistente de valores de cores sólidas.

## Conversão do espaço de cores {#section-ca87b80b8e364ea59d8a92d87121b0fb}

O Servidor de imagens geralmente tenta atrasar as conversões de cores durante o processamento. Se todas as camadas de uma imagem tiverem o mesmo espaço de cores de camada, a conversão para o espaço de cores de saída será feita após a mesclagem e o dimensionamento final. Se vários espaços de cores de camada estiverem envolvidos, cada camada será transformada no espaço de cores de saída antes da mesclagem.

>[!NOTE]
>
>Os comandos `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` e `op_saturation=` são operações do RGB. Essas operações mantêm a fidelidade de cores somente se o espaço de cores da camada tiver o tipo de pixel RGB. Se forem diferentes do RGB, os dados serão convertidos para o RGB usando a conversão de cores ingênua e o resultado terá fidelidade de cores limitada. O espaço de cores da camada para essas camadas deve ser considerado indeterminado.

As opções de conversão de cores são fornecidas com `icc=` ou, se `icc=` não for especificado, com `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` e `attribute::IccDither`.

## Como incorporar perfis de cores {#section-261ebbae5ce046589a776ca972380052}

O perfil de cores ICC do espaço de cores de saída, se disponível, pode ser incorporado à imagem de resposta especificando `iccEmbed=`.

## Gerenciamento de perfis ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Todos os perfis de cores usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC normalmente têm um sufixo de arquivo [!DNL .icc] ou [!DNL .icm] e estão co-localizados com arquivos de dados de imagem.

Embora os perfis de saída possam ser especificados por caminho/nome de arquivo no comando `icc=`, é recomendável registrar todos os arquivos de perfil no Mapa de Perfil ICC do catálogo padrão ou do catálogo de imagens e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Todos os perfis ICC referenciados em `catalog::IccProfile` e em `attribute::IccProfile*` devem ser registrados no Mapa de Perfis ICC da imagem ou catálogo padrão.

## Restrições {#section-fb50ede40b124b89b30679da29782ab5}

Somente espaços de cores CMYK, RGB e tons de cinza são suportados no momento.

## Perfis de cores ICC incluídos {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

O Servidor de imagens inclui a maioria dos perfis padrão do Adobe ICC no catálogo de imagens padrão. Esses perfis podem ser acessados por seus nomes comuns (por exemplo, como visto no Photoshop) ou com um identificador um pouco mais curto. A tabela a seguir lista todos os perfis ICC padrão. Ao referenciar um perfil no comando `icc=` por seu nome comum, os espaços devem ser codificados como `%20`.

Perfis adicionais podem ser adicionados aos perfis padrão, no catálogo padrão ou em um catálogo de imagens específico. Consulte a [Referência do Mapa de Perfil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) para obter detalhes.

>[!NOTE]
>
>A tabela a seguir se aplica somente ao *Dynamic Media Hybrid* (em execução no modo de execução `dynamicmedia`).

| Identificador | Nome comum | Nome do arquivo |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | RGB CIE | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Espaço de Cores sRgb Profile.icm |
| `WideGamutRGB` | RGB de gamut amplo | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | FOGRA27 revestido (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 revestida (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | GRACoL 2006 revestido (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa ISO Revestido FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Revestimento Euroscale | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale não revestido v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japão Colorido 2001 Revestido | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Jornal Japan Color 2002 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japão Colorido 2001 Sem Revestimento | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Revestimento Para Web No Japão (Anúncio) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | Papel de jornal dos EUA (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 Padrão CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMYK padrão do Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed sem revestimento v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 sem revestimento (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 revestida com web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Papel revestido para web SWOP 2006 Grade 3 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Papel revestido para web SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | Web sem revestimento dos EUA v2 | USWebUncoated.icc |

A tabela a seguir se aplica ao *Servidor de imagens do Dynamic Media Classic* e ao *Dynamic Media* (em execução no modo de execução `dynamicmedia_scene7`).

| Identificador | Nome comum | Nome do arquivo |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Espaço de Cores sRgb Profile.icm |
| `WideGamutRGB` | RGB de gamut amplo | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | FOGRA27 revestido (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 revestida (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | GRACoL 2006 revestido (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa ISO Revestido FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale não revestido v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japão Colorido 2001 Revestido | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Jornal Japan Color 2002 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japão Colorido 2001 Sem Revestimento | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Revestimento Para Web No Japão (Anúncio) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 Padrão CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMYK padrão do Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed sem revestimento v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 sem revestimento (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | Papel de jornal dos EUA (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 revestida com web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Papel revestido para web SWOP 2006 Grade 3 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Papel revestido para web SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | Web sem revestimento dos EUA v2 | USWebUncoated.icc |

## Consulte também {#section-39159397e80b4efca5f631eab8b9aa06}

[Consórcio Internacional de Cores](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
