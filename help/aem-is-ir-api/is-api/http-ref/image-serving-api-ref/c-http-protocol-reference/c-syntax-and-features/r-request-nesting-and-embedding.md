---
description: O Serviço de Imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de Imagens, incorporação de solicitações de Renderização de Imagens e incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada são compatíveis com esses mecanismos.
seo-description: O Serviço de Imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de Imagens, incorporação de solicitações de Renderização de Imagens e incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada são compatíveis com esses mecanismos.
seo-title: Solicitar aninhamento e incorporação
solution: Experience Manager
title: Solicitar aninhamento e incorporação
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# Solicitar aninhamento e incorporação{#request-nesting-and-embedding}

O Serviço de Imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de Imagens, incorporação de solicitações de Renderização de Imagens e incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada são compatíveis com esses mecanismos.

>[!NOTE]
>
>Determinados clientes de email e servidores proxy podem codificar as chaves usadas para a sintaxe de aninhamento e incorporação. Os aplicativos para os quais isso é um problema devem usar parênteses em vez de chaves.

## Solicitações de exibição de imagem aninhada {#section-6954202119e0466f8ff27c79f4f039c8}

Uma solicitação de Exibição de imagem inteira pode ser usada como uma fonte de camada ao especificá-la no comando `src=` (ou `mask=`) usando a seguinte sintaxe:

`…&src=is( nestedRequest)&…`

O token `is` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do servidor (normalmente ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Efetivamente, as solicitações aninhadas devem ser codificadas da mesma forma que a solicitação externa (de aninhamento).

As regras de pré-processamento são aplicadas às solicitações aninhadas.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se a imagem resultante das solicitações aninhadas incluir dados de máscara (alfa), ela será passada para a camada de incorporação como máscara de camada.

Também são ignoradas `attribute::MaxPix`e `attribute::DefaultPix` do catálogo de imagem que se aplica à solicitação aninhada.

O resultado da imagem de uma solicitação IS aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada num pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização de imagem incorporadas {#section-69c5548db930412b9b90d9b2951a6969}

Quando a Renderização de imagem do Dynamic Media está ativada no servidor, as solicitações de renderização podem ser usadas como fontes de camada, especificando-as no comando src= (ou mask=). Use a seguinte sintaxe:

` …&src=ir( *[!DNL renderRequest]*)&…`

O token `ir` diferencia maiúsculas de minúsculas.

*[!DNL renderRequest]* é a solicitação comum de Renderização de imagem, excluindo o caminho raiz HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Com efeito, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (de incorporação).

Os seguintes comandos de Renderização de imagem são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada num pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização FXG incorporadas {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando o renderizador de gráficos FXG (também conhecido como [!DNL AGMServer]) é instalado e ativado com o Image Serving, as solicitações FXG podem ser usadas como fontes de camada especificando-as em comandos `src=` (ou `mask=`). Use a seguinte sintaxe:

`…&src=fxg( renderRequest)&…`

O token `fxg` diferencia maiúsculas de minúsculas.

>[!NOTE]
>
>A renderização de gráficos FXG está disponível somente no ambiente hospedado da Dynamic Media e pode exigir licenciamento adicional. Entre em contato com o suporte técnico da Dynamic Media para obter mais informações.

*[!DNL renderRequest]* é a solicitação de renderização FXG normal, excluindo o caminho raiz HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Com efeito, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (de incorporação).

Os seguintes comandos FXG são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fontes de imagem externas {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

O Serviço de Imagens suporta acesso a imagens de origem em servidores HTTP estrangeiros.

>[!NOTE]
>
>Somente o protocolo HTTP é compatível com URLs remotos.

Para especificar um URL externo para um comando `src=` ou `mask=`, delimite o fragmento de URL ou URL externo com parênteses:

`…&src=( foreignUrl)&…`

Importante: os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Com efeito, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (de incorporação).

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Um erro ocorre se um URL absoluto for incorporado e o atributo : `AllowDirectUrls` é 0 ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

Embora URLs estrangeiros não possam ser especificados diretamente no componente de caminho do URL da solicitação, é possível configurar uma regra de pré-processamento para permitir a conversão de caminhos relativos em URLs absolutos (consulte o exemplo abaixo).

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP. Se nem um `ETag` nem um cabeçalho de resposta HTTP Last-Modified estiver presente, a resposta não será armazenada em cache. Isso pode causar um desempenho ruim para acessos repetidos da mesma imagem externa, pois o Serviço de Imagens precisa buscar novamente e revalidar a imagem em cada acesso.

Esse mecanismo suporta os mesmos formatos de arquivo de imagem que são compatíveis com o utilitário Conversão de Imagem (IC), com exceção das imagens de origem com 16 bits por componente.

>[!NOTE]
>
>O Image Serving executará automaticamente o utilitário validate quando uma imagem estrangeira é usada pela primeira vez, para garantir que a imagem é válida e não foi corrompida durante a transmissão. Isso pode causar um pequeno atraso no primeiro acesso. Para melhor desempenho, é recomendável limitar o tamanho dessas imagens e/ou usar um formato de arquivo de imagem que comprima bem.

## Restrições {#section-fb68e3f0d40947feb94d7bf183b64929}

O tamanho da imagem gerada por solicitações aninhadas/incorporadas é normalmente otimizado automaticamente. Se o armazenamento em cache de imagens de solicitação aninhadas estiver ativado, os ganhos de desempenho incrementais poderão ser alcançados especificando o tamanho exato da imagem aninhada, de modo que não será necessário mais dimensionamento quando a entrada do cache for reutilizada.

O Serviço de imagem importante não oferece suporte à codificação dupla de solicitações aninhadas ou incorporadas. As solicitações aninhadas e incorporadas devem ser codificadas por HTTP como solicitações simples.

## Exemplos {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modelo de camadas com armazenamento em cache:**

Use o aninhamento para adicionar armazenamento em cache a um modelo de camadas. Um número limitado de imagens de plano de fundo é sobreposto por um texto altamente variável. A string inicial do modelo pode ter esta aparência:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Com pequenas modificações, podemos pré-dimensionar a imagem da camada 0 e armazená-la em cache de forma persistente, reduzindo assim a carga do servidor:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Como incorporar solicitações de renderização de imagem do Dynamic Media**

Usar um modelo armazenado em [!DNL myCatalog/myTemplate]; gere a imagem para a camada 2 do modelo usando a Renderização de imagem do Dynamic Media:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Observe as chaves aninhadas. A solicitação de Renderização de imagem incorpora uma chamada de volta ao Serviço de imagem para recuperar uma textura repetível.

## Consulte também {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Solicitar pré-processamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Referência de renderização de imagem,  [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Utilitários de veiculação de  [imagem](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
