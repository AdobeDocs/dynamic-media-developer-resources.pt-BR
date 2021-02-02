---
description: O Serviço de imagens oferece suporte a conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).
solution: Experience Manager
title: Gerenciamento de cores do Serviço de imagens
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---


# Gerenciamento de cores do serviço de imagens{#image-serving-color-management}

O Serviço de imagens oferece suporte a conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).

## Espaços de cor padrão {#section-8cfe60808bce49968091995e4e521dba}

Cada catálogo de imagens (e o catálogo padrão) pode definir um conjunto de perfis ICC que constituem os espaços de cor padrão para esse catálogo - uma entrada e um perfil de saída cada para dados em escala cinza, RGB e CMYK. Consulte ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)` e ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espaço de cor de entrada {#section-9f08e2c1b6aa4fe4815be174972c1944}

As imagens de origem podem incorporar perfis ICC para definir o espaço de cor de entrada. Se nenhum perfil estiver incorporado em uma imagem de origem, `attribute::IccProfileSrc*` do catálogo de imagem aplicável correspondente ao tipo de pixel da imagem de origem será usado. Se esse atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` será usado. Se esse atributo do catálogo também não estiver definido, a imagem não será gerenciada por cores e apenas transformações ingênuas serão aplicadas.

## Espaço de cor de saída {#section-b517bca622b64dcfa7defba6035d0716}

O espaço de cores do resultado final da imagem de uma solicitação é definido com o comando `icc=`. Se `icc=` não for especificado, o espaço de cor de saída padrão (do catálogo principal da solicitação) que corresponde ao tipo de pixel da imagem de saída será usado como o espaço de cor de saída. Se nenhum perfil de saída for definido no catálogo principal ou padrão e se a camada base for uma imagem com um perfil incorporado que corresponda ao tipo de pixel de saída, esse perfil será usado para o espaço de cor de saída. Caso contrário, o espaço de cores de saída permanecerá indefinido — somente conversões de cores ingênuas serão aplicadas ao converter entre tipos de pixels e nenhum perfil de cores poderá ser incorporado na imagem de saída.

O espaço de cores de saída de uma solicitação aninhada/incorporada do Serviço de imagem é sempre o mesmo que o espaço de cores de saída da solicitação externa e de incorporação.

## Cores sólidas {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Os valores de cor especificados com `color=`, `bgcolor=` ou o comando RTF `\iscolortbl` serão associados ao espaço de cores de entrada se o valor de cor incluir o sufixo &#39;S&#39;, caso contrário, serão associados ao espaço de cores de saída. Os valores de cor especificados com `bgc=` ou os comandos RTF `\colortbl` e `\cmykcolortbl` estão sempre associados ao espaço de cor de saída padrão ou real correspondente.

>[!NOTE]
>
>No momento, `bgc=` não participa totalmente no gerenciamento de cores - o sufixo &#39;S&#39; é ignorado quando especificado com `bgc=`, e a conversão ingênua é aplicada quando o tipo de pixel do valor de cor especificado com `bgc=` é diferente do tipo de pixel da imagem de saída. Caso contrário, `bgc=` está associado ao espaço de cor de saída real.

## Solicitações aninhadas e incorporadas {#section-bdda638c31504f26a77e51ebb1ea6e3b}

O espaço de cor de saída para solicitações IS aninhadas e solicitações IR incorporadas é automaticamente definido para o espaço de cor de saída da solicitação mais externa, a menos que a solicitação aninhada especifique um espaço de cor de saída explícito com `icc=`. Além disso, as solicitações aninhadas/incorporadas também herdam os espaços de cores de saída padrão do catálogo principal da solicitação mais externa, para garantir o manuseio consistente dos valores de cor sólida.

## Conversão de espaço de cores {#section-ca87b80b8e364ea59d8a92d87121b0fb}

O Serviço de imagem geralmente tenta atrasar as conversões de cores durante o processamento. Se todas as camadas de uma imagem tiverem o mesmo espaço de cor da camada, a conversão para o espaço de cor de saída será feita após a mesclagem e a escala final. Se vários espaços de cor de camada estiverem envolvidos, cada camada será transformada no espaço de cor de saída antes da mesclagem.

>[!NOTE]
>
>Os comandos `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` e `op_saturation=` são operações RGB. Essas operações mantêm a fidelidade da cor somente se o espaço de cor da camada tiver o tipo de pixel RGB. Se não for RGB, os dados serão convertidos em RGB usando conversão de cores ingênua e o resultado terá fidelidade de cores limitada. O espaço de cor da camada para essas camadas deve ser considerado indeterminado.

As opções de conversão de cores são fornecidas com `icc=` ou, se `icc=` não for especificado, com `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` e `attribute::IccDither`.

## Incorporação de perfis de cor {#section-261ebbae5ce046589a776ca972380052}

O perfil de cor ICC do espaço de cor de saída, se disponível, pode ser incorporado à imagem de resposta especificando `iccEmbed=`.

## Gerenciando perfis ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Todos os perfis coloridos usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC normalmente têm um sufixo de arquivo [!DNL .icc] ou [!DNL .icm] e são co-localizados com arquivos de dados de imagem.

Embora os perfis de saída possam ser especificados pelo caminho/nome do arquivo no comando `icc=`, recomenda-se registrar todos os arquivos de perfil no Mapa de Perfis ICC do catálogo padrão ou catálogo de imagens e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Todos os perfis ICC referenciados em `catalog::IccProfile` e em `attribute::IccProfile*` devem ser registrados no Mapa de Perfis ICC da imagem ou catálogo padrão.

## Restrições {#section-fb50ede40b124b89b30679da29782ab5}

No momento, apenas os espaços de cores CMYK, RGB e escala de cinza são suportados.

## Perfis de cor ICC incluídos {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

O Serviço de imagem inclui a maioria dos perfis Adobe ICC padrão no catálogo de imagens padrão. Esses perfis podem ser acessados por seus nomes comuns (por exemplo, como visto no Photoshop) ou por um identificador um pouco mais curto. A tabela a seguir lista todos os perfis ICC padrão. Ao referenciar um perfil no comando `icc=` pelo nome comum, os espaços devem ser codificados como `%20`.

Perfis adicionais podem ser adicionados aos perfis padrão, tanto no catálogo padrão quanto em um catálogo de imagens específico. Consulte [Referência do mapa de Perfis ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) para obter detalhes.

>[!NOTE]
>
>A tabela a seguir se aplica somente a *Dynamic Media Hybrid* (em execução no modo de execução `dynamicmedia`).

|Identificador|Nome comum|Nome do arquivo|
|— |— |— |
|**RGB**||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|Perfil Rgb Color Space.icm|
|`WideGamutRGB`|Gamut largo RGB|WideGamutRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|COated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europa ISO Revestido FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Revestimento Euroscale|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncovered v2|EuroscaleUncovered.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Jornal Japan Color 2002|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 UnRevestido|JapanColor2001Não Revestido.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|Jornal dos EUA (SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|CMYK padrão Photoshop 4|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|EUA Revestido com Placa v2|USSheetfeedCoated.icc|
|`SheetfedUncoated`|EUA Placa alimentada sem revestimento v2|USSheetfeedUncovered.icc|
|`UncoatedFogra29`|FOGRA29 sem revestimento (ISO 12647-2:2004)|Não revestidoFOGRA29.icc|
|`WebCoated`|EUA Revestido da Web (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Papel SWOP Revestido na Web 2006 Grau 3|Papel WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Papel SWOP Revestido na Web 2006 Grau 5|Papel WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|EUA Web sem revestimento v2|USWebUncovered.icc|

A tabela a seguir se aplica a *Dynamic Media Classic Image Serving* e *Dynamic Media* (em execução no modo de execução `dynamicmedia_scene7`).

|Identificador|Nome comum|Nome do arquivo|
|— |— |— |
|**RGB**||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|Perfil Rgb Color Space.icm|
|`WideGamutRGB`|Gamut largo RGB|WideGamutRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|COated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europa ISO Revestido FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Revestimento Euroscale v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncovered v2|EuroscaleUncovered.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Jornal Japan Color 2002|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 UnRevestido|JapanColor2001Não Revestido.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|CMYK padrão Photoshop 4|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|EUA Revestido com Placa v2|USSheetfeedCoated.icc|
|`SheetfedUncoated`|EUA Placa alimentada sem revestimento v2|USSheetfeedUncovered.icc|
|`UncoatedFogra29`|FOGRA29 sem revestimento (ISO 12647-2:2004)|Não revestidoFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|Jornal dos EUA (SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|EUA Revestido da Web (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Papel SWOP Revestido na Web 2006 Grau 3|Papel WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Papel SWOP Revestido na Web 2006 Grau 5|Papel WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|EUA Web sem revestimento v2|USWebUncovered.icc|

## Consulte também {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [atributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*,  [atributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*,  [atributo::IccRenderIntentIntent, IcccAttribute::IccPointNegroCompensação](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)  [ ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Indicador:Icc OutraPerfil, Referência do Mapa de  do ICC,cor=, bgc=3000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
