---
description: O Serviço de Imagens implementa um simples recurso de marca d'água visual.
seo-description: O Serviço de Imagens implementa um simples recurso de marca d'água visual.
seo-title: Marcas d'água
solution: Experience Manager
title: Marcas d'água
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Marcas d&#39;água{#watermarks}

O Serviço de Imagens implementa um simples recurso de marca d&#39;água visual.

Uma marca d&#39;água normalmente é uma imagem semitransparente, mas pode ser um texto ou uma imagem composta em camadas mais complexa. O servidor colocará a marca d&#39;água sobre a imagem de resposta depois que todos os atributos de visualização ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) forem aplicados.

A marca d&#39;água é ativada ao configurar `attribute::Watermark` para uma entrada de catálogo válida que conteria a imagem ou o modelo da marca d&#39;água. Se `attribute::Watermark` estiver definido em um catálogo nomeado, o servidor adicionará a marca d&#39;água a todas as solicitações de imagem que referenciarem a ID do catálogo no URL da solicitação. Se `default::Watermark` estiver definido (no catálogo padrão, [!DNL default.ini]), a marca d&#39;água será aplicada a todas as solicitações de imagem, independentemente de referenciarem ou não um catálogo.

As marcas d&#39;água não são aplicadas a imagens retornadas em resposta a solicitações em miniatura ( `req=tmb`) e a determinadas solicitações dos visualizadores do Scene7.

## Dimensionamento e alinhamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando uma marca d&#39;água é especificada, o servidor gera primeiro a imagem composta (a *imagem do público alvo*) à qual a marca d&#39;água precisa ser aplicada (antes de aplicar as transformações da visualização). Em seguida, o servidor gera a imagem composta para a marca d&#39;água como qualquer outra imagem (a *imagem de marca d&#39;água*).

Diferentemente das imagens padrão, `sizeN=` pode ser especificado para layer=0 ou layer=comp da imagem de marca d&#39;água. Isso permite o dimensionamento da imagem da marca d&#39;água em relação à imagem do público alvo. Se `sizeN=` não for especificado, a imagem da marca d&#39;água manterá seu tamanho de pixel ao ser unida à imagem do público alvo.

Os comandos de solicitação (como `fmt=`) e os comandos de visualização (como `wid=`) são ignorados nos registros de marca d&#39;água, com exceção de `align=`. `align=` pode ser usado para posicionar a imagem da marca d&#39;água em relação à imagem da marca d&#39;água em relação à imagem do público alvo. Isso permite o posicionamento da marca d&#39;água em relação a um canto ou borda da imagem do público alvo.

Depois de dimensionar e alinhar, o servidor colocará a imagem da marca d&#39;água sobre a imagem do público alvo usando os valores `blendMode=` e `opac=` especificados para `layer=0` ou `layer=comp` da imagem da marca d&#39;água. Finalmente, os comandos de solicitação e visualização especificados para a imagem do público alvo são aplicados para construir a imagem de resposta.

Observe que a imagem de marca d&#39;água nunca se estenderá por nenhum espaço em branco adicionado à imagem de resposta pelos comandos `wid=` e `hei=`.

## Exemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Uma marca d&#39;água típica pode consistir em uma imagem RGBA simples contendo um logotipo ou um aviso de copyright. Criamos um registro no catálogo de imagens (ou no catálogo padrão) com `catalog::Id` definido como `watermark` e especificamos o arquivo de imagem de marca d&#39;água em `catalog::Path`. Queremos esticar a marca d&#39;água para ajustar a imagem da visualização (sem distorcer a marca d&#39;água), deixando uma margem extra, e reduzir a opacidade para 20% da marca d&#39;água original, portanto definimos `catalog::Modifier` como `sizeN=0.9,0.9&opac=20`. Para ativar a marca d&#39;água, defina `attribute::Watermark` para a id da entrada do catálogo de marca d&#39;água, &quot;marca d&#39;água&quot; neste exemplo. Talvez queiramos experimentar diferentes `blendMode=` escolhas para obter diferentes efeitos de marca d&#39;água.

## Consulte também {#section-4d66713abacb42c7b6a0c93cbf966a97}

[atributo::Marca d&#39;água](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
