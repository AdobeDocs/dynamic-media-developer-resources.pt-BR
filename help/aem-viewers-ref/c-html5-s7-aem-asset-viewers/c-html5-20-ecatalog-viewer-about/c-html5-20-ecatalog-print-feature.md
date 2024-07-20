---
title: Recurso de impressão
description: O visualizador permite exibir o conteúdo do catálogo em uma impressora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Recurso de impressão{#print-feature}

O visualizador permite exibir o conteúdo do catálogo em uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Não é recomendável configurar `printquality` para valores maiores que o padrão. Isso ocorre porque ele leva a um alto consumo de memória pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso de impressão só está disponível em sistemas desktop, exceto no Internet Explorer 9.
