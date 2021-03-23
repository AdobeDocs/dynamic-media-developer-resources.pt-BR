---
description: Análise JPEG progressiva. O JPEG progressivo exibe uma imagem de forma que ele inicialmente mostre uma foto borrada/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela fica mais clara à medida que os dados da imagem são baixados com mais facilidade. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.
seo-description: Análise JPEG progressiva. O JPEG progressivo exibe uma imagem de forma que ele inicialmente mostre uma foto borrada/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela fica mais clara à medida que os dados da imagem são baixados com mais facilidade. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.
seo-title: scan
solution: Experience Manager
title: scan
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# scan{#pscan}

Análise JPEG progressiva. O JPEG progressivo exibe uma imagem de forma que ele inicialmente mostre uma foto borrada/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela fica mais clara à medida que os dados da imagem são baixados com mais facilidade. Esse parâmetro permite definir o número de verificações necessárias (3, 4 ou 5) para que a imagem inteira seja exibida.

`pscan=auto|3|4|5`

A velocidade real de cada varredura depende da velocidade de transmissão do sistema do usuário e do computador que recebe e descompacta os dados.

`Auto` O usa as configurações de digitalização computadas pela biblioteca JPEG independente e depende do modelo de cores. Os valores de `3`, `4`, `5` correspondem à configuração de Digitalização encontrada no Adobe Photoshop quando você salva um arquivo JPEG como um pjpeg (JPEG progressivo).

Se `pscan` não estiver definido, o padrão será `auto`.

## Propriedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se o formato de saída não for JPEG progressivo.

## Padrão {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Consulte também {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
