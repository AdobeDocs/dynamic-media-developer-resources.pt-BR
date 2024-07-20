---
title: descartar
description: Referência da API do JavaScript para o Visualizador de imagem de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# descartar{#dispose}

Referência da API do JavaScript para o Visualizador de imagem de vídeo.

`dispose()`

Descarta essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador no tempo de execução.

O código da página da Web também deve excluir a variável da instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de eventos diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas para esses componentes, esses ouvintes deverão ter o registro cancelado explicitamente pelo código da página da Web. Essas referências de componentes externos devem ser excluídas antes de chamar `dispose()`.

Não acesse mais a API do Visualizador depois que `dispose()` for chamado.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
