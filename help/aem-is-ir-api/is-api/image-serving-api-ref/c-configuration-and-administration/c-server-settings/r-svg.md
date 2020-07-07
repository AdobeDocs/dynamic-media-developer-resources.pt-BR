---
description: As configurações nesta seção precisam ser consideradas somente se a renderização SVG for necessária.
seo-description: As configurações nesta seção precisam ser consideradas somente se a renderização SVG for necessária.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# SVG{#svg}

As configurações nesta seção precisam ser consideradas somente se a renderização SVG for necessária.

## SV::SvgHeapSize - Tamanho do Heap SVG {#section-59ab17681daa4be8b5d794713e1a504e}

O tamanho do heap do Java para o renderizador SVG. O padrão é &quot;200m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - Pastas raiz de dados SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

A localização dos arquivos de dados de origem SVG. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Normalmente definido para o mesmo valor de `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Tamanho máximo do arquivo SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamanho máximo do arquivo de origem SVG em kBytes. O servidor retorna um erro quando é feita uma tentativa de renderizar um arquivo SVG maior que esse limite. O padrão é 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - Limite de Tamanho de Imagem de Saída SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita o tamanho das imagens que SVGRender pode produzir. Valor inteiro maior que 0 em milhões de pixels. Um erro será retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 4.

## PS::svgProvider.port - Porta de escuta do Platform Server {#section-f7e42a96c2dd4523b46f0557c239e659}

A porta usada para SvgRender obter imagens do Platform Server para serem incorporadas em renderizações SVG.

Importante Para o funcionamento correto do componente SVGRender, essa opção de configuração deve ser definida com o mesmo valor `TC::PsPort`.

## PS::svgProvider.fontRoot - Pasta de arquivos de fonte SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica onde o SvgRender encontrará os arquivos de fonte necessários para renderizar o texto SVG; normalmente um dos caminhos especificados em `IS::RootPaths`. O padrão é [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta de comunicações SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura a porta na qual o Servidor de imagens e o componente SVGRender se comunicam.

>[!NOTE]
>
>Para o funcionamento correto do componente SVGRender, o mesmo número de porta deve ser especificado para `SVG::SVGRender.port` e `IS::SVGTcpPort`.

