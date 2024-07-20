---
description: O Servidor de imagens implementa um recurso simples de marca d'água visual.
solution: Experience Manager
title: Marcas d'água
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Marcas d&#39;água{#watermarks}

O Servidor de imagens implementa um recurso simples de marca d&#39;água visual.

Uma marca d&#39;água normalmente é uma imagem semitransparente, mas pode ser um texto ou uma imagem composta em camadas mais complexa. O servidor coloca a marca d&#39;água em camadas sobre a imagem de resposta depois que todos os atributos de exibição ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) forem aplicados.

A marca d&#39;água está habilitada ao configurar `attribute::Watermark` para uma entrada de catálogo válida que conteria a imagem da marca d&#39;água ou o modelo. Se `attribute::Watermark` estiver definido em um catálogo nomeado, o servidor adicionará a marca d&#39;água a todas as solicitações de imagem que referenciam a ID do catálogo na URL da solicitação. Se `default::Watermark` estiver definido (no catálogo padrão, [!DNL default.ini]), a marca d&#39;água será aplicada a todas as solicitações de imagem, independentemente de referenciarem ou não um catálogo.

As marcas d&#39;água não são aplicadas a imagens retornadas em resposta a solicitações de miniatura ( `req=tmb`) e a determinadas solicitações de visualizadores do Dynamic Media.

## Dimensionamento e alinhamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando uma marca d&#39;água é especificada, o servidor gera primeiro a imagem composta (a *imagem de destino*) à qual a marca d&#39;água precisa ser aplicada (antes de aplicar as transformações de exibição). O servidor então gera a imagem composta para a marca d&#39;água como qualquer outra imagem (a *imagem de marca d&#39;água*).

Ao contrário das imagens padrão, `sizeN=` pode ser especificado para layer=0 ou layer=comp da imagem da marca d&#39;água. Isso permite o dimensionamento da imagem da marca d&#39;água em relação à imagem de destino. Se `sizeN=` não for especificado, a imagem da marca d&#39;água manterá seu tamanho de pixel ao ser mesclada com a imagem de destino.

Os comandos Request (como `fmt=`) e view (como `wid=`) são ignorados em registros de marca d&#39;água, com exceção de `align=`. `align=` pode ser usado para posicionar a imagem da marca d&#39;água relativa à imagem da marca d&#39;água relativa à imagem de destino. Isso permite o posicionamento da marca d&#39;água em relação a um canto ou borda da imagem de destino.

Após dimensionar e alinhar, o servidor coloca a imagem da marca d&#39;água em camadas sobre a imagem de destino usando os valores `blendMode=` e `opac=` especificados para `layer=0` ou `layer=comp` da imagem da marca d&#39;água. Finalmente, os comandos request e view especificados para a imagem de destino são aplicados para construir a imagem de resposta.

Observe que a imagem de marca d&#39;água nunca se estende por nenhum espaço em branco adicionado à imagem de resposta pelos comandos `wid=` e `hei=`.

## Exemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Uma marca d&#39;água típica pode consistir em uma imagem RGBA simples contendo um logotipo ou um aviso de copyright. Criamos um registro no catálogo de imagens (ou no catálogo padrão) com `catalog::Id` definido como `watermark` e especificamos o arquivo de imagem de marca d&#39;água em `catalog::Path`. Queremos alongar a marca d&#39;água para ajustá-la à imagem da exibição (sem distorcer a marca d&#39;água), deixando uma margem extra e reduzindo a opacidade para 20% da marca d&#39;água original, para que definamos `catalog::Modifier` como `sizeN=0.9,0.9&opac=20`. Para ativar a marca d&#39;água, defina `attribute::Watermark` como a ID da entrada do catálogo da marca d&#39;água, &quot;marca d&#39;água&quot; neste exemplo. Podemos experimentar com diferentes `blendMode=` escolhas para obter diferentes efeitos de marca d&#39;água.

## Consulte também {#section-4d66713abacb42c7b6a0c93cbf966a97}

[atributo::marca d&#39;água](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
