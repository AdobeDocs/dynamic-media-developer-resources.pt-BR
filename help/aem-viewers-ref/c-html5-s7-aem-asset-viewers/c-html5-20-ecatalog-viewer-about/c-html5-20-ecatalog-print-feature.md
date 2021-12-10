---
title: Recurso Imprimir
description: O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Recurso Imprimir{#print-feature}

O visualizador permite que você faça a saída do conteúdo do catálogo para uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada com a `printquality` parâmetro de configuração. Configuração `printquality` não são recomendados valores superiores ao padrão. O motivo é porque leva a alto consumo de memória pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o configurado `printquality` valor.

>[!NOTE]
>
>O recurso Imprimir só está disponível em sistemas de desktop, exceto no Internet Explorer 9.
