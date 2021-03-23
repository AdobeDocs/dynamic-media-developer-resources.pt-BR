---
description: O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.
seo-description: O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.
seo-title: Recurso Imprimir
solution: Experience Manager
title: Recurso Imprimir
uuid: 4932042a-1421-4589-8bf5-88bbe38d774d
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Imprimir recurso{#print-feature}

O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Observe que não é recomendado configurar `printquality` para valores significativamente maiores que o padrão. O motivo é porque leva a um consumo de memória muito alto pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso Imprimir só está disponível em sistemas de desktop, exceto no Internet Explorer 9.

