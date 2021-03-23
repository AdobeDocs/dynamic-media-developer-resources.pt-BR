---
description: O Serviço de Imagens implementa um recurso simples de marcas d'água visuais.
solution: Experience Manager
title: Marcas d'água
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Marcas d&#39;água{#watermarks}

O Serviço de Imagens implementa um recurso simples de marcas d&#39;água visuais.

Uma marca d&#39;água geralmente é uma imagem semitransparente, mas pode ser um texto ou uma imagem composta mais complexa e em camadas. O servidor colocará a marca d&#39;água em camada sobre a imagem de resposta depois que todos os atributos de exibição ( `wid=`, `hei=`, `align=`, `scl=`) tiverem sido aplicados.`bgc=`

A marca d&#39;água é ativada ao definir `attribute::Watermark` para uma entrada de catálogo válida que conteria a imagem ou o modelo da marca d&#39;água. Se `attribute::Watermark` for definido em um catálogo nomeado, o servidor adicionará a marca d&#39;água a todas as solicitações de imagem que referenciam a id do catálogo no URL da solicitação. Se `default::Watermark` for definido (no catálogo padrão, [!DNL default.ini]), a marca d&#39;água será aplicada a todas as solicitações de imagem, independentemente de referenciarem ou não um catálogo.

As marcas d&#39;água não são aplicadas a imagens retornadas em resposta a solicitações de miniatura ( `req=tmb`) e a determinadas solicitações dos visualizadores do Dynamic Media.

## Dimensionamento e alinhamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando uma marca d&#39;água é especificada, o servidor primeiro gerará a imagem composta (a *imagem do target*) à qual a marca d&#39;água precisa ser aplicada (antes de aplicar as transformações de exibição). O servidor então gera a imagem composta para a marca d&#39;água como qualquer outra imagem (a *imagem da marca d&#39;água*).

Diferentemente das imagens padrão, `sizeN=` pode ser especificado para layer=0 ou layer=comp da imagem da marca d&#39;água. Isso permite dimensionar a imagem da marca d&#39;água em relação à imagem de destino. Se `sizeN=` não for especificado, a imagem da marca d&#39;água manterá seu tamanho de pixel ao ser unida à imagem de destino.

Os comandos de solicitação (como `fmt=`) e os comandos de exibição (como `wid=`) são ignorados nos registros de marca d&#39;água, com exceção de `align=`. `align=` pode ser usada para posicionar a imagem da marca d&#39;água em relação à imagem da marca d&#39;água em relação à imagem de destino. Isso permite o posicionamento da marca d&#39;água em relação a um canto ou borda da imagem de destino.

Após dimensionar e alinhar, o servidor irá colocar a imagem da marca d&#39;água em camadas sobre a imagem de destino usando os valores `blendMode=` e `opac=` especificados para `layer=0` ou `layer=comp` da imagem da marca d&#39;água. Finalmente, os comandos request e view especificados para a imagem de destino são aplicados para criar a imagem de resposta.

Observe que a imagem da marca d&#39;água nunca se estenderá por nenhum espaço em branco adicionado à imagem de resposta pelos comandos `wid=` e `hei=`.

## Exemplo {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Uma marca d&#39;água típica pode consistir em uma imagem RGBA simples contendo um logotipo ou um aviso de copyright. Criamos um registro no catálogo de imagens (ou no catálogo padrão) com `catalog::Id` definido como `watermark` e especificamos o arquivo de imagem da marca d&#39;água em `catalog::Path`. Queremos esticar a marca d&#39;água para ajustar a imagem da exibição (sem distorcer a marca d&#39;água), deixando uma margem extra, e reduzir a opacidade para 20% da marca d&#39;água original, então definimos `catalog::Modifier` como `sizeN=0.9,0.9&opac=20`. Para ativar a marca d&#39;água, defina `attribute::Watermark` para a id da entrada do catálogo de marca d&#39;água, &quot;marca d&#39;água&quot; neste exemplo. Talvez queiramos experimentar opções diferentes de `blendMode=` para obter efeitos diferentes de marca d&#39;água.

## Consulte também {#section-4d66713abacb42c7b6a0c93cbf966a97}

[atributo::Marca d&#39;água](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
