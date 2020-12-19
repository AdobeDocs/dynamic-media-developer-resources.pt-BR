---
description: Análise progressiva de JPEG. O JPEG progressivo exibe uma imagem de tal forma que mostra inicialmente uma foto indefinida/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela se torna mais clara à medida que os dados da imagem são baixados. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.
seo-description: Análise progressiva de JPEG. O JPEG progressivo exibe uma imagem de tal forma que mostra inicialmente uma foto indefinida/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela se torna mais clara à medida que os dados da imagem são baixados. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.
seo-title: scan
solution: Experience Manager
title: scan
topic: Scene7 Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# pscan{#pscan}

Análise progressiva de JPEG. O JPEG progressivo exibe uma imagem de tal forma que mostra inicialmente uma foto indefinida/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela se torna mais clara à medida que os dados da imagem são baixados. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.

`pscan=auto|3|4|5`

A velocidade real de cada varredura depende da velocidade de transmissão do sistema do usuário e do computador que recebe e descompacta os dados.

`Auto` usa as configurações de digitalização computadas pela biblioteca JPEG independente e dependem do modelo de cores. Os valores de `3`, `4`, `5` correspondem à configuração de Digitalização encontrada no Adobe Photoshop quando você salva um arquivo JPEG como pjpeg (JPEG progressivo).

Se `pscan` não estiver definido, o padrão será `auto`.

## Propriedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo de solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se o formato de saída não for JPEG progressivo.

## Padrão {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Consulte também {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
