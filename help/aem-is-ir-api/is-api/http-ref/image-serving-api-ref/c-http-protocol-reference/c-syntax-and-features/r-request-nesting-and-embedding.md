---
description: O Servidor de imagens oferece suporte ao aninhamento ilimitado de solicitações do Servidor de imagens, à incorporação de solicitações de Renderização de imagens e à incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens e máscaras de camada suportam esses mecanismos.
solution: Experience Manager
title: Aninhamento e incorporação de solicitações
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Aninhamento e incorporação de solicitações{#request-nesting-and-embedding}

O Servidor de imagens oferece suporte ao aninhamento ilimitado de solicitações do Servidor de imagens, à incorporação de solicitações de Renderização de imagens e à incorporação de imagens recuperadas de servidores estrangeiros. Somente imagens e máscaras de camada suportam esses mecanismos.

>[!NOTE]
>
>Determinados clientes de email e servidores proxy podem codificar as chaves usadas para a sintaxe de aninhamento e incorporação. Os aplicativos para os quais isso é um problema devem usar parênteses em vez de chaves.

## Solicitações de disponibilização de imagens aninhadas {#section-6954202119e0466f8ff27c79f4f039c8}

Uma solicitação inteira do Servidor de imagens pode ser usada como uma origem de camada especificando-a no comando `src=` (ou `mask=`) usando esta sintaxe:

`…&src=is( nestedRequest)&…`

O token `is` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do servidor (normalmente ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados em HTTP. Com efeito, as solicitações aninhadas devem ser codificadas da mesma forma que a solicitação externa (aninhamento).

As regras de pré-processamento são aplicadas a solicitações aninhadas.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (na URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se a imagem resultante das solicitações aninhadas incluir dados de máscara (alfa), ela será passada para a camada de incorporação como a máscara de camada.

Também são ignorados `attribute::MaxPix`e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação aninhada.

O resultado da imagem de uma solicitação IS aninhada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização de imagem inseridas {#section-69c5548db930412b9b90d9b2951a6969}

Quando a Renderização de imagem do Dynamic Media está ativada no servidor, as solicitações de renderização podem ser usadas como fontes de camada ao especificá-las no comando src= (ou mask=). Use a seguinte sintaxe:

` …&src=ir( *[!DNL renderRequest]*)&…`

O token `ir` diferencia maiúsculas de minúsculas.

*[!DNL renderRequest]* é a solicitação usual de Renderização de Imagem, excluindo o caminho raiz HTTP ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Os caracteres delimitadores de solicitação aninhados ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) nas solicitações aninhadas não devem ser codificados em HTTP. Na prática, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

Os seguintes comandos de Renderização de imagem são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação de IR aninhada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

## Solicitações de renderização FXG inseridas {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando o renderizador de gráficos FXG (também conhecido como [!DNL AGMServer]) é instalado e habilitado com o Servidor de Imagens, as solicitações FXG podem ser usadas como fontes de camada especificando-as nos comandos `src=` (ou `mask=`). Use a seguinte sintaxe:

`…&src=fxg( renderRequest)&…`

O token `fxg` diferencia maiúsculas de minúsculas.

>[!NOTE]
>
>A renderização de gráficos FXG está disponível somente no ambiente hospedado pela Dynamic Media e pode exigir licenciamento adicional. Entre em contato com o suporte técnico da Dynamic Media para obter mais informações.

*[!DNL renderRequest]* é a solicitação de renderização FXG normal, excluindo o caminho raiz HTTP ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) em solicitações aninhadas não devem ser codificados em HTTP. Na prática, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

Os seguintes comandos FXG são ignorados quando especificados em solicitações aninhadas:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Fontes de imagem estrangeiras {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

O Servidor de imagens oferece suporte ao acesso a imagens de origem em servidores HTTP estrangeiros.

>[!NOTE]
>
>Somente o protocolo HTTP é compatível com URLs remotos.

Para especificar uma URL externa para um comando `src=` ou `mask=`, delimite a URL externa ou o fragmento de URL com parênteses:

`…&src=( foreignUrl)&…`

Importante: os caracteres delimitadores ( `'(',')'`) e os caracteres delimitadores de comando ( `'?'`, `'&'`, `'='`) em solicitações aninhadas não devem ser codificados em HTTP. Na prática, as solicitações incorporadas devem ser codificadas da mesma forma que a solicitação externa (incorporação).

URLs absolutos completos (se `attribute::AllowDirectUrls` estiver definido) e URLs relativos a `attribute::RootUrl` são permitidos. Erro se uma URL absoluta estiver inserida e o atributo: `AllowDirectUrls` for 0, ou se uma URL relativa for especificada e `attribute::RootUrl` estiver vazia.

Embora URLs estrangeiros não possam ser especificados diretamente no componente de caminho do URL de solicitação, é possível configurar uma regra de pré-processamento para permitir a conversão de caminhos relativos em URLs absolutos (consulte o exemplo abaixo).

Imagens estrangeiras são armazenadas em cache pelo servidor de acordo com os cabeçalhos de cache incluídos na resposta HTTP. Se nenhum cabeçalho de resposta HTTP `ETag` ou Last-Modified estiver presente, a resposta não será armazenada em cache. Isso pode causar baixo desempenho para acessos repetidos para a mesma imagem externa, já que o Servidor de imagens precisa buscar novamente e revalidar a imagem em cada acesso.

Esse mecanismo aceita os mesmos formatos de arquivo de imagem compatíveis com o utilitário Image Convert (IC), com exceção das imagens de origem com 16 bits por componente.

>[!NOTE]
>
>O Servidor de imagens executa automaticamente o utilitário de validação quando uma imagem externa é usada pela primeira vez, para garantir que a imagem seja válida e não tenha sido corrompida durante a transmissão. Isso pode causar um pequeno atraso no primeiro acesso. Para obter o melhor desempenho, é recomendável limitar o tamanho dessas imagens e/ou usar um formato de arquivo de imagem que seja bem compactado.

## Restrições {#section-fb68e3f0d40947feb94d7bf183b64929}

O tamanho da imagem gerada por solicitações aninhadas/incorporadas normalmente é otimizado automaticamente. Se o armazenamento em cache de imagens de solicitação aninhadas estiver ativado, podem ser obtidos ganhos de desempenho incrementais especificando o tamanho exato da imagem aninhada, de modo que não seja necessário dimensionamento adicional quando a entrada de cache for reutilizada.

Importante O Servidor de imagens não oferece suporte à codificação dupla de solicitações aninhadas ou incorporadas. As solicitações aninhadas e inseridas devem ser codificadas em HTTP, como as solicitações simples.

## Exemplos {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modelo de camada com cache:**

Use o aninhamento para adicionar armazenamento em cache a um modelo em camada. Um número limitado de imagens de fundo são sobrepostas por texto altamente variável. A cadeia de caracteres do modelo inicial pode ser semelhante a:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Com pequenas modificações, podemos pré-dimensionar a imagem da camada 0 e armazená-la em cache de forma persistente, reduzindo assim a carga do servidor:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporando solicitações para Renderização de Imagem Dynamic Media**

Usando um modelo armazenado em [!DNL myCatalog/myTemplate]; gere a imagem para a camada 2 do modelo usando a Renderização de Imagem Dynamic Media:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Observe as chaves aninhadas. A solicitação de Renderização de imagem incorpora uma chamada de retorno ao Servidor de imagens para recuperar uma textura repetível.

## Consulte também {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Solicitar Pré-Processamento](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Referência de Renderização de Imagem, [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Utilitários de Servidor de Imagens](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
