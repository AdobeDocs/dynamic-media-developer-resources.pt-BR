---
description: O Serviço de imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de imagens, à incorporação de solicitações de Renderização de imagens, bem como à incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada suportam esses mecanismos.
seo-description: O Serviço de imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de imagens, à incorporação de solicitações de Renderização de imagens, bem como à incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada suportam esses mecanismos.
seo-title: Solicitação de aninhamento e incorporação
solution: Experience Manager
title: Solicitação de aninhamento e incorporação
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---


# Solicitar aninhamento e incorporação{#request-nesting-and-embedding}

O Serviço de imagens oferece suporte ao aninhamento ilimitado de solicitações do Serviço de imagens, à incorporação de solicitações de Renderização de imagens, bem como à incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens de camada e máscaras de camada suportam esses mecanismos.

>[!NOTE]
>
>Determinados clientes de email e servidores proxy podem codificar as chaves usadas para a sintaxe de aninhamento e incorporação. Os aplicativos para os quais isso é um problema devem usar parênteses em vez de chaves.

## Solicitações aninhadas do serviço de imagem {#section-6954202119e0466f8ff27c79f4f039c8}

Uma solicitação de Serviço de imagem inteira pode ser usada como uma fonte de camada, especificando-a no comando `src=` (ou `mask=`) usando a seguinte sintaxe:

`…&src=is( nestedRequest)&…`

O token `is` faz distinção entre maiúsculas e minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do servidor (normalmente ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Efetivamente, as solicitações aninhadas devem ser codificadas da mesma forma que a solicitação externa (aninhamento).

As regras de pré-processamento são aplicadas a solicitações aninhadas.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se a imagem resultante das solicitações aninhadas incluir dados de máscara (alfa), ela será passada para a camada de incorporação como máscara de camada.

Também são ignorados `attribute::MaxPix`e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação aninhada.

O resultado da imagem de uma solicitação IS aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente dentro de um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização de imagem incorporadas {#section-69c5548db930412b9b90d9b2951a6969}

Quando a Renderização de imagem do Dynamic Media está ativada no servidor, as solicitações de renderização podem ser usadas como fontes de camada, especificando-as no comando src= (ou mask=). Use a seguinte sintaxe:

` …&src=ir( *[!DNL renderRequest]*)&…`

O token `ir` faz distinção entre maiúsculas e minúsculas.

*[!DNL renderRequest]* é a solicitação comum de renderização de imagem, excluindo o caminho raiz HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Efetivamente, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

Os seguintes comandos de Renderização de imagem são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente dentro de um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização FXG incorporadas {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando o renderizador de gráficos FXG (também conhecido como [!DNL AGMServer]) é instalado e ativado com o Serviço de Imagens, as solicitações FXG podem ser usadas como fontes de camada especificando-as nos comandos `src=` (ou `mask=`). Use a seguinte sintaxe:

`…&src=fxg( renderRequest)&…`

O token `fxg` faz distinção entre maiúsculas e minúsculas.

>[!NOTE]
>
>A renderização de gráficos FXG está disponível somente no ambiente hospedado da Dynamic Media e pode exigir licenciamento adicional. Entre em contato com o suporte técnico da Dynamic Media para obter mais informações.

*[!DNL renderRequest]* é a solicitação de renderização FXG comum, excluindo o caminho raiz HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Efetivamente, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

Os seguintes comandos FXG são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fontes de imagem externas {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

O Serviço de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP externos.

>[!NOTE]
>
>Somente o protocolo HTTP é compatível com URLs remotos.

Para especificar um URL externo para um comando `src=` ou `mask=`, delimite o fragmento de URL ou URL externo com parênteses:

`…&src=( foreignUrl)&…`

Importante Os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados por HTTP. Efetivamente, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` serão permitidos. Ocorre um erro se um URL absoluto for incorporado e o atributo: `AllowDirectUrls` é 0, ou se um URL relativo é especificado e `attribute::RootUrl` está vazio.

Embora URLs externos não possam ser especificados diretamente no componente de caminho do URL da solicitação, é possível configurar uma regra de pré-processamento para permitir a conversão de caminhos relativos em URLs absolutos (consulte o exemplo abaixo).

As imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP. Se nenhum cabeçalho de resposta HTTP `ETag` ou Last-Modifid estiver presente, a resposta não será armazenada em cache. Isso pode causar um desempenho ruim para acessos repetidos para a mesma imagem externa, já que o Serviço de imagem precisa buscar novamente e revalidar a imagem em cada acesso.

Este mecanismo suporta os mesmos formatos de arquivo de imagem suportados pelo utilitário Conversão de imagem (IC), com exceção das imagens de origem com 16 bits por componente.

>[!NOTE]
>
>O Serviço de imagem executará automaticamente o utilitário de validação quando uma imagem estrangeira for usada pela primeira vez, para garantir que a imagem seja válida e não tenha sido corrompida durante a transmissão. Isso pode causar um pequeno atraso no primeiro acesso. Para obter o melhor desempenho, é recomendável limitar o tamanho dessas imagens e/ou usar um formato de arquivo de imagem que compacte bem.

## Restrições {#section-fb68e3f0d40947feb94d7bf183b64929}

O tamanho da imagem gerada por solicitações aninhadas/incorporadas é normalmente otimizado automaticamente. Se o armazenamento em cache de imagens de solicitação aninhadas estiver ativado, os ganhos de desempenho incrementais podem ser alcançados especificando o tamanho exato da imagem aninhada, para que não seja necessário dimensionar mais quando a entrada do cache for reutilizada.

O Serviço de imagem importante não suporta a codificação de duplos de solicitações aninhadas ou incorporadas. As solicitações aninhadas e incorporadas devem ser codificadas por HTTP da mesma forma que as solicitações simples.

## Exemplos {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modelo de layout com cache:**

Use o aninhamento para adicionar cache a um modelo de camadas. Um número limitado de imagens de plano de fundo é sobreposto por um texto altamente variável. A string inicial do modelo pode ser semelhante a esta:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Com pequenas modificações, podemos pré-dimensionar a imagem da camada 0 e armazená-la em cache de forma persistente, reduzindo assim a carga do servidor:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporação de solicitações para renderização de imagem do Dynamic Media**

Usando um modelo armazenado em [!DNL myCatalog/myTemplate]; gere a imagem para a camada2 do modelo usando a Renderização de imagem do Dynamic Media:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Observe as chaves aninhadas. A solicitação de renderização de imagem incorpora uma chamada de volta ao Serviço de imagem para recuperar uma textura repetível.

## Consulte também {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Solicitar pré-processamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Referência de renderização de imagem,  [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Utilitários de  [disponibilização de imagem](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
