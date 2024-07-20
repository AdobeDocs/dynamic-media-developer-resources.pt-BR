---
description: O visualizador permite exibir o conteúdo do catálogo em uma impressora.
solution: Experience Manager
title: Recurso de impressão
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Recurso de impressão{#print-feature}

O visualizador permite exibir o conteúdo do catálogo em uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Observe que não é recomendado configurar `printquality` para valores significativamente maiores que o padrão. Isso ocorre porque ele leva a um consumo de memória muito alto pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso de impressão só está disponível em sistemas desktop, exceto no Internet Explorer 9.
