---
description: As configurações nesta seção só precisam ser consideradas se a renderização de SVG for necessária.
seo-description: As configurações nesta seção só precisam ser consideradas se a renderização de SVG for necessária.
seo-title: SVG
solution: Experience Manager
title: SVG
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# SVG{#svg}

As configurações nesta seção só precisam ser consideradas se a renderização de SVG for necessária.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

O tamanho do heap Java do renderizador SVG. O padrão é &quot;200m&quot; (200 Mbytes).

## PS::svgProvider.rootPaths - Pastas raiz de dados SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

O local dos arquivos de dados de origem SVG. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto e vírgula. Normalmente, é definido com o mesmo valor de `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Tamanho máximo do arquivo SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Tamanho máximo do arquivo de origem SVG em kBytes. O servidor retorna um erro quando é feita uma tentativa de renderizar um arquivo SVG maior que esse limite. O padrão é 1024 kbytes.

## IS::SvgMAxRenderRgnPixels - Limite de Tamanho da Imagem de Saída SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita o tamanho das imagens que o SVGRender pode produzir. Valor inteiro maior que 0 em milhões de pixels. Um erro é retornado se uma operação de renderização exceder o limite de tamanho. O padrão é 4.

## PS::svgProvider.port - Porta de escuta do servidor de plataforma {#section-f7e42a96c2dd4523b46f0557c239e659}

A porta usada para o SvgRender obter imagens do Servidor de plataforma para serem incorporadas em renderizações de SVG.

Importante Para o funcionamento correto do componente SVGRender, essa opção de configuração deve ser definida com o mesmo valor que `TC::PsPort`.

## PS::svgProvider.fontRoot - Pasta de arquivos de fonte SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Especifica onde o SvgRender encontrará os arquivos de fonte necessários para renderizar o texto SVG; normalmente um dos caminhos especificados em `IS::RootPaths`. O padrão é [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta de Comunicações SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura a porta na qual o Servidor de Imagem e o componente SVGRender se comunicam.

>[!NOTE]
>
>Para o funcionamento correto do componente SVGRender, o mesmo número de porta deve ser especificado para `SVG::SVGRender.port` e `IS::SVGTcpPort`.

