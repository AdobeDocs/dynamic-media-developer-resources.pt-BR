---
description: O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.
solution: Experience Manager
title: Recurso Imprimir
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Recurso Imprimir{#print-feature}

O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Observe que não é recomendado configurar `printquality` para valores significativamente maiores que o padrão. O motivo é porque leva a um consumo de memória muito alto pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso Imprimir só está disponível em sistemas de desktop, exceto no Internet Explorer 9.
