---
title: init
description: Referência da API do JavaScript para o Visualizador de Zoom em Linha.
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

Referência da API do JavaScript para o Visualizador de Zoom em Linha.

`init()`

Inicia a inicialização do visualizador para que o código do visualizador possa encontrá-lo por sua ID. Nesse momento, o elemento DOM do contêiner deve ser criado.

Se o elemento do contêiner ainda não fizer parte do layout da página da Web - por exemplo, ele pode estar oculto usando `display:none` estilo atribuído a ele - o visualizador suspende seu processo de inicialização. Isso ocorre até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

Chamar esse método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência para a instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
