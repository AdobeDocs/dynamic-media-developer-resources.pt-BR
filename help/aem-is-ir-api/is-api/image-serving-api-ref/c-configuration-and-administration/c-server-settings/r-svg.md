---
description: As configurações desta seção precisam ser consideradas somente se a renderização de SVG for necessária.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# SVG{#svg}

As configurações desta seção precisam ser consideradas somente se a renderização de SVG for necessária.

## SV::SvgHeapSize - Tamanho do heap de SVG {#section-59ab17681daa4be8b5d794713e1a504e}

O tamanho do heap de Java do Renderizador de SVG. O padrão é &quot;200m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - Pastas de Raiz de Dados SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

O local dos arquivos de dados de origem do SVG. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Normalmente definida com o mesmo valor de `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Tamanho Máximo do Arquivo SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamanho máximo do arquivo de origem de SVG em kBytes. O servidor retorna um erro quando é feita uma tentativa de renderizar um arquivo de SVG que é maior do que esse limite. O padrão é 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - Limite de Tamanho da Imagem de Saída de SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita o tamanho das imagens que o SVGRender pode produzir. Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 4.

## PS::svgProvider.port - [!DNL Platform Server] Porta de escuta {#section-f7e42a96c2dd4523b46f0557c239e659}

A porta usada por SvgRender para obter imagens do [!DNL Platform Server] para ser incorporado nas renderizações de SVG.

Importante Para o funcionamento correto do componente SVGRender, essa opção de configuração deve ser definida com o mesmo valor que `TC::PsPort`.

## PS::svgProvider.fontRoot - Pasta de arquivos de fontes SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica onde o SvgRender encontrará os arquivos de fonte necessários para renderizar o texto SVG; normalmente, um dos caminhos especificados em `IS::RootPaths`. O padrão é [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta de Comunicação SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura a porta em que o Servidor de imagens e o componente SVGRender se comunicam.

>[!NOTE]
>
>Para o funcionamento correto do componente SVGRender, o mesmo número de porta deve ser especificado para `SVG::SVGRender.port` e `IS::SVGTcpPort`.
