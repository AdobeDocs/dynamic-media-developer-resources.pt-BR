---
title: pscan
description: Análise de JPEG progressiva. O JPEG progressivo exibe uma imagem de forma que inicialmente mostra uma foto indefinida/de baixa qualidade em sua totalidade.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# pscan{#pscan}

Análise de JPEG progressiva. O JPEG progressivo exibe uma imagem de forma que inicialmente mostra uma foto indefinida/de baixa qualidade em sua totalidade. À medida que a digitalização continua, ela se torna mais clara à medida que os dados da imagem são baixados. Esse parâmetro permite que você defina o número de digitalizações que são feitas (3, 4 ou 5) para a imagem inteira aparecer.

`pscan=auto|3|4|5`

A velocidade real de cada varredura depende da velocidade de transmissão do sistema do usuário e do computador que recebe e descompacta os dados.

`Auto` O usa as configurações de digitalização computadas pela biblioteca de JPEG independente e que dependem do modelo de cores. Os valores de `3`, `4`, `5` corresponde à configuração Digitalização encontrada no Adobe Photoshop quando você salva um arquivo JPEG como pjpeg (JPEG progressivo).

Se `pscan` não estiver definido, o padrão será `auto`.

## Propriedades {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Solicitar atributo. Aplica-se independentemente da configuração da camada atual. Ignorado se o formato de saída não for JPEG progressivo.

## Padrão {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemplo {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Consulte também {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
