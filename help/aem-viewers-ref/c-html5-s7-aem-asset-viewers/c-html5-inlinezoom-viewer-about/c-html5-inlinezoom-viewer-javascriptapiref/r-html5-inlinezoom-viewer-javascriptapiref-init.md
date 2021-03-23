---
description: Referência da API do JavaScript para o Visualizador de Zoom em Linha.
seo-description: Referência da API do JavaScript para o Visualizador de Zoom em Linha.
seo-title: init
solution: Experience Manager
title: init
uuid: a3bd0cd1-e4cb-4b09-a78f-0958b55a79e4
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# init{#init}

Referência da API do JavaScript para o Visualizador de Zoom em Linha.

`init()`

Inicia a inicialização do visualizador para que o código do visualizador possa encontrá-lo por sua ID. Nesse momento, o elemento DOM do contêiner deve ser criado.

Se o elemento do contêiner ainda não fizer parte do layout da página da Web (por exemplo, pode ser oculto usando o estilo `display:none` atribuído a ele), o visualizador suspende o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Chamar esse método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência para a instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

