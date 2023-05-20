---
title: init
description: Referência da API JavaScript para o Visualizador de zoom em linha.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# init{#init}

Referência da API JavaScript para o Visualizador de zoom em linha.

`init()`

Inicia a inicialização do visualizador para que o código do visualizador possa encontrá-lo por sua ID. Nesse momento, o elemento DOM do contêiner deve ser criado.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web - por exemplo, ele pode estar oculto usando `display:none` estilo atribuído a ele - o visualizador suspende o processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
