---
description: O Servidor de imagens implementa um recurso simples de marca d'água visual.
solution: Experience Manager
title: Marcas d'água
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Marcas d&#39;água{#watermarks}

O Servidor de imagens implementa um recurso simples de marca d&#39;água visual.

Uma marca d&#39;água normalmente é uma imagem semitransparente, mas pode ser um texto ou uma imagem composta em camadas mais complexa. O servidor colocará a marca d&#39;água sobre a imagem de resposta após todos os atributos de visualização ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) foram aplicadas.

A marca d&#39;água é ativada pela configuração `attribute::Watermark` para uma entrada de catálogo válida que conteria a imagem ou o modelo da marca d&#39;água. Se `attribute::Watermark` for definido em um catálogo nomeado, o servidor adicionará a marca d&#39;água a todas as solicitações de imagem que fazem referência à id do catálogo no URL da solicitação. Se `default::Watermark` está definido (no catálogo padrão, [!DNL default.ini]), a marca d&#39;água é aplicada a todas as solicitações de imagem, independentemente de referenciarem ou não um catálogo.

As marcas d&#39;água não são aplicadas a imagens retornadas em resposta a solicitações de miniatura ( `req=tmb`) e determinadas solicitações de visualizadores do Dynamic Media.

## Dimensionamento e alinhamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando uma marca d&#39;água é especificada, o servidor primeiro gerará a imagem composta (a variável *imagem de destino*) ao qual a marca d&#39;água precisa ser aplicada (antes da aplicação das transformações de visualização). Em seguida, o servidor gera a imagem composta para a marca d&#39;água como qualquer outra imagem (a *imagem da marca d&#39;água*).

Ao contrário das imagens padrão, `sizeN=` pode ser especificado para layer=0 ou layer=comp da imagem da marca d&#39;água. Isso permite o dimensionamento da imagem da marca d&#39;água em relação à imagem de destino. Se `sizeN=` não for especificada, a imagem de marca d&#39;água manterá seu tamanho de pixel ao ser mesclada com a imagem de destino.

Comandos de solicitação (como `fmt=`) e comandos de visualização (como `wid=`) são ignorados em registros de marca d&#39;água, com exceção de `align=`. `align=` pode ser usado para posicionar a imagem da marca d&#39;água em relação à imagem da marca d&#39;água em relação à imagem de destino. Isso permite o posicionamento da marca d&#39;água em relação a um canto ou borda da imagem de destino.

Após o dimensionamento e o alinhamento, o servidor criará uma camada da imagem da marca d&#39;água sobre a imagem de destino usando o `blendMode=` e `opac=` valores especificados para `layer=0` ou `layer=comp` da imagem da marca d&#39;água. Finalmente, os comandos request e view especificados para a imagem de destino são aplicados para construir a imagem de resposta.

Observe que a imagem da marca d&#39;água nunca se estenderá por nenhum espaço em branco adicionado à imagem de resposta pelo `wid=` e `hei=` comandos.

## Exemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Uma marca d&#39;água típica pode consistir em uma imagem RGBA simples contendo um logotipo ou um aviso de copyright. Criamos um registro no catálogo de imagens (ou no catálogo padrão) com `catalog::Id` definir como `watermark` e especifique o arquivo de imagem de marca d&#39;água em `catalog::Path`. Queremos alongar a marca d&#39;água para ajustá-la à imagem da exibição (sem distorcer a marca d&#39;água), deixando uma pequena margem extra e reduzindo a opacidade para 20% da marca d&#39;água original, então definimos `catalog::Modifier` para `sizeN=0.9,0.9&opac=20`. Para ativar a marca d&#39;água, defina `attribute::Watermark` para a id da entrada do catálogo de marca d&#39;água, &quot;marca d&#39;água&quot; neste exemplo. Podemos querer experimentar com diferentes `blendMode=` para obter diferentes efeitos de marca d&#39;água.

## Consulte também {#section-4d66713abacb42c7b6a0c93cbf966a97}

[atributo::marca d&#39;água](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
