---
description: Referência da API JavaScript para o Visualizador de vídeo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: 2ee5bddc-957c-4813-9285-d64b9ac7d590
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

Referência da API JavaScript para o Visualizador de vídeo.

`init()`

Start a inicialização do Visualizador de vídeo. Nesse momento, o elemento DOM do container deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento container ainda não fizer parte do layout da página da Web, por exemplo, ele pode estar oculto usando o estilo `display:none` atribuído a ele, o visualizador suspende seu processo de inicialização até o momento em que a página da Web traz o elemento container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Chame este método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

