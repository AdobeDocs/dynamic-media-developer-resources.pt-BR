---
description: O Image Serving suporta conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).
solution: Experience Manager
title: Gerenciamento de cores do fornecimento de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Gerenciamento de cores do fornecimento de imagens{#image-serving-color-management}

O Image Serving suporta conversões de espaço de cores com base em perfis de espaço de cores que estão em conformidade com a especificação ICC (International Color Consortium).

## Espaços de cores padrão {#section-8cfe60808bce49968091995e4e521dba}

Cada catálogo de imagem (e o catálogo padrão) pode definir um conjunto de perfis ICC que constituem os espaços de cores padrão para esse catálogo - uma entrada e um perfil de saída cada para dados em escala cinza, RGB e CMYK. Consulte ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`e ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espaço de cores de entrada {#section-9f08e2c1b6aa4fe4815be174972c1944}

Imagens de origem podem incorporar perfis ICC para definir o espaço de cores de entrada. Se nenhum perfil for incorporado em uma imagem de origem, `attribute::IccProfileSrc*` do catálogo de imagens aplicável correspondente ao tipo de pixel da imagem de origem é usado. Se este atributo não estiver definido no catálogo de imagens, `attribute::IccProfile*` é usada. Se esse atributo de catálogo também não estiver definido, a imagem não será gerenciada por cores e apenas transformações ingênuas serão aplicadas.

## Espaço de cores de saída {#section-b517bca622b64dcfa7defba6035d0716}

O espaço de cores do resultado final da imagem de uma solicitação é definido com a variável `icc=` comando. If `icc=` não for especificado, o espaço de cores de saída padrão (do catálogo principal da solicitação) que corresponde ao tipo de pixel da imagem de saída será usado como o espaço de cores de saída. Se nenhum perfil de saída for definido no catálogo principal ou padrão e se a camada base for uma imagem com um perfil incorporado correspondente ao tipo de pixel de saída, esse perfil será usado para o espaço de cores de saída. Caso contrário, o espaço de cores de saída permanecerá indefinido — somente conversões de cores ingênuas são aplicadas ao converter entre tipos de pixels e nenhum perfil de cores pode ser incorporado na imagem de saída.

O espaço de cores de saída de uma solicitação aninhada/incorporada de Exibição de Imagens é sempre o mesmo que o espaço de cores de saída da solicitação externa de incorporação.

## Cores sólidas {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Valores de cor especificados com `color=`, `bgcolor=`ou o comando RTF `\iscolortbl` são associadas ao espaço de cores de entrada se o valor de cor incluir o sufixo &#39;S&#39;; caso contrário, são associadas ao espaço de cores de saída. Valores de cor especificados com `bgc=` ou os comandos RTF `\colortbl` e `\cmykcolortbl` estão sempre associadas ao espaço de cores padrão ou de saída real correspondente.

>[!NOTE]
>
>Nesse momento, `bgc=` não participa totalmente no gerenciamento de cores - o sufixo &#39;S&#39; é ignorado quando especificado com `bgc=`, e a conversão ingênua é aplicada quando o tipo de pixel do valor de cor especificado com `bgc=` difere do tipo de pixel da imagem de saída. Caso contrário, `bgc=` está associada ao espaço de cores de saída real.

## Solicitações aninhadas e incorporadas {#section-bdda638c31504f26a77e51ebb1ea6e3b}

O espaço de cores de saída para solicitações IS aninhadas e solicitações IR incorporadas é automaticamente definido para o espaço de cores de saída da solicitação mais externa, a menos que a solicitação aninhada especifique um espaço de cores de saída explícito com `icc=`. Além disso, as solicitações aninhadas/incorporadas também herdam os espaços de cores de saída padrão do catálogo principal da solicitação mais externa, para garantir o manuseio consistente de valores de cores sólidas.

## Conversão do espaço de cores {#section-ca87b80b8e364ea59d8a92d87121b0fb}

O Image Serving geralmente tenta atrasar conversões de cores durante o processamento. Se todas as camadas de uma imagem tiverem o mesmo espaço de cor de camada, a conversão para o espaço de cores de saída será feita após a união e o dimensionamento final. Se vários espaços de cores de camada estiverem envolvidos, cada camada será transformada no espaço de cores de saída antes da mesclagem.

>[!NOTE]
>
>Os comandos `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`e `op_saturation=` são operações de RGB. Essas operações mantêm a fidelidade de cores somente se o espaço de cores da camada tiver o tipo de RGB pixel. Se não for RGB, os dados serão convertidos em RGB usando conversão de cores ingênua e o resultado terá fidelidade de cores limitada. O espaço de cor da camada para essas camadas deve ser considerado indeterminado.

As opções de conversão de cores são fornecidas com `icc=` ou, se `icc=` não especificado, com `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`e `attribute::IccDither`.

## Como incorporar perfis de cores {#section-261ebbae5ce046589a776ca972380052}

O perfil de cores ICC do espaço de cores de saída, se disponível, pode ser incorporado à imagem de resposta especificando `iccEmbed=`.

## Gerenciamento de perfis ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Todos os perfis de cores usados pelo servidor devem estar em conformidade com a especificação ICC. Os arquivos de perfil ICC geralmente têm um [!DNL .icc] ou [!DNL .icm] sufixo do arquivo e são co-localizados com arquivos de dados de imagem.

Embora os perfis de saída possam ser especificados pelo caminho/nome do arquivo na `icc=` , é recomendável registrar todos os arquivos de perfil no Mapa de Perfil ICC do catálogo ou catálogo de imagem padrão e usar identificadores de atalho ( `icc::Name`) em vez de caminhos de arquivo.

Todos os perfis ICC referenciados em `catalog::IccProfile` e `attribute::IccProfile*` deve ser registrado no Mapa de Perfil ICC da imagem ou no catálogo padrão.

## Restrições {#section-fb50ede40b124b89b30679da29782ab5}

Somente os espaços de cores CMYK, RGB e escala de cinza são suportados no momento.

## Perfis de cores ICC incluídos {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

A Exibição de imagens inclui a maioria dos perfis Adobe ICC padrão no catálogo de imagens padrão. Esses perfis podem ser acessados por seus nomes comuns (como visto no Photoshop) ou com um identificador um pouco mais curto. A tabela a seguir lista todos os perfis ICC padrão. Ao fazer referência a um perfil no `icc=` por seu nome comum, os espaços devem ser codificados como `%20`.

Perfis adicionais podem ser adicionados aos perfis padrão, seja no catálogo padrão ou em um catálogo de imagem específico. Consulte a [Referência do mapa de perfis ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) para obter detalhes.

>[!NOTE]
>
>A tabela a seguir se aplica a *Dynamic Media Híbrido* somente (executando em `dynamicmedia` modo de execução).

|Identificador|Nome comum|Nome do arquivo| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|Apple RGB|AppleRGB.icc| |`CIERGB`|CIE RGB|CIERGB.icc| |`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|ProPhoto RGB|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|Perfil de Espaço de Cor do Rgb.icm| |`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc| |**CMYK**|| |`CoatedFogra27`|Revestido FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|Revestido FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`CoatedGraCol`|GRACoL 2006 revestido (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Não Revestido v2|EuroscaleUnported.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`Jornal japonês Color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Japão Color 2001 UnRevestido|JapãoColor2001UnRevestido.icc| |`JapanColorWebCoated`|Japão Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japão Web Coated (Ad)|JapanWebCoated.icc| |`NewsprintSNAP2007`|Jornal dos EUA (SNAP 2007)|USNewsprintSNAP2007.icc| |`PS4Default`CMYK padrão do Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK Padrão do Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|EUA Revestido com Folha v2|USSheetfeedCoated.icc| |`SheetfedUncoated`|EUA Sem Revestimento com Folha v2|USSheetfeedUnpurchased.icc| |`UncoatedFogra29`|FOGRA29 não revestida (ISO 12647-2:2004)|Não revestidaFOGRA29.icc| |`WebCoated`|EUA Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`WebCoatedGrade3`|Papel Web Coated SWOP 2006 Grau 3|WebCoatedSWOP2006Grade3.icc| |`WebCoatedGrade5`|Papel Web Coated SWOP 2006 Grau 5|WebCoatedSWOP2006Grade5.icc| |`WebUncoated`|EUA Web não revestida v2|USWebUnpurchased.icc|

A tabela a seguir se aplica a *Dynamic Media Classic Image Serving* e *Dynamic Media* (executando em `dynamicmedia_scene7` modo de execução).

|Identificador|Nome comum|Nome do arquivo| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|Apple RGB|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|Perfil de Espaço de Cor do Rgb.icm| |`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc| |**CMYK**|| |`CoatedFogra27`|Revestido FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|Revestido FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|GRACoL 2006 revestido (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Não Revestido v2|EuroscaleUnported.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`Jornal japonês Color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Japão Color 2001 UnRevestido|JapãoColor2001UnRevestido.icc| |`Japan Color 2003 Web Coated`|Japão Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japão Web Coated (Ad)|JapanWebCoated.icc| |`PS4Default`CMYK padrão do Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK Padrão do Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|EUA Revestido com Folha v2|USSheetfeedCoated.icc| |`SheetfedUncoated`|EUA Sem Revestimento com Folha v2|USSheetfeedUnpurchased.icc| |`UncoatedFogra29`|FOGRA29 não revestida (ISO 12647-2:2004)|Não revestidaFOGRA29.icc| |`US Newsprint (SNAP 2007)`|Jornal dos EUA (SNAP 2007)|USNewsprintSNAP2007.icc| |`WebCoated`|EUA Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`|Papel Web Coated SWOP 2006 Grau 3|WebCoatedSWOP2006Grade3.icc| |`Web Coated SWOP Grade 5 Paper`|Papel Web Coated SWOP 2006 Grau 5|WebCoatedSWOP2006Grade5.icc| |`WebUncoated`|EUA Web não revestida v2|USWebUnpurchased.icc|

## Consulte também {#section-39159397e80b4efca5f631eab8b9aa06}

[Consórcio Internacional de Cores](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [atributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, [atributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*, [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccBlackPointCompensação](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [atributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [Referência do mapa de perfis ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
