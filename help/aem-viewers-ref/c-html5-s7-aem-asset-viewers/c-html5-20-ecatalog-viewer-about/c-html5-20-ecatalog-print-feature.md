---
description: O visualizador permite que você imprima o conteúdo do catálogo para uma impressora.
seo-description: O visualizador permite que você imprima o conteúdo do catálogo para uma impressora.
seo-title: Recurso Imprimir
solution: Experience Manager
title: Recurso Imprimir
topic: Dynamic Media
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Recurso de impressão{#print-feature}

O visualizador permite que você imprima o conteúdo do catálogo para uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Observe que não é recomendado configurar `printquality` para valores significativamente superiores ao padrão. O motivo é que leva a um consumo de memória muito alto pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para a empresa do Dynamic Media Classic é maior do que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso Imprimir só está disponível em sistemas de desktop, exceto no Internet Explorer 9.

