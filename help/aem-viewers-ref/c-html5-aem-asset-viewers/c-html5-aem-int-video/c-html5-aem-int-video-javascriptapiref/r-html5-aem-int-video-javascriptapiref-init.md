---
description: Referência da API do JavaScript para o Visualizador de vídeo interativo.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de vídeo interativo.

`init()`

Inicia a inicialização do Visualizador de vídeo interativo. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento do contêiner ainda não fizer parte do layout da página da Web (por exemplo, pode ser oculto usando o estilo `display:none` atribuído a ele), o visualizador suspende o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência para a instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
