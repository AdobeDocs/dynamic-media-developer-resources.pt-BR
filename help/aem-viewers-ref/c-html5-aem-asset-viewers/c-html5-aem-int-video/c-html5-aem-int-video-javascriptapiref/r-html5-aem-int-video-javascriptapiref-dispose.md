---
description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-title: dispor
solution: Experience Manager
title: dispor
topic: Dynamic Media
uuid: 95046b8c-1277-4954-b13d-329994d0cb04
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# dispor{#dispose}

Referência da API JavaScript para o Visualizador de vídeo interativo.

`dispose()`

Descarta essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador em tempo de execução.

O código da página da Web também deve excluir a variável de instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de evento diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas a esses componentes, esses ouvintes deverão ser explicitamente não registrados pelo código da página da Web, e essas referências de componentes externos deverão ser excluídas antes de chamar `dispose()`.

Não acesse mais a API do visualizador depois que `dispose()` for chamado.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

