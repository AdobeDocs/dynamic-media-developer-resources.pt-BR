---
description: Referência da API do JavaScript para o Visualizador de mídia mista.
solution: Experience Manager
title: dispor
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,User
exl-id: e09f73a9-a961-4188-b092-f7bbcae4946d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# dispor{#dispose}

Referência da API do JavaScript para o Visualizador de mídia mista.

`dispose()`

Dispõe essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador em tempo de execução.

O código da página da Web também deve excluir a variável da instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de eventos diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas a esses componentes, esses ouvintes deverão ser explicitamente cancelados pelo código da página da Web, e essas referências de componentes externos deverão ser excluídas antes de chamar `dispose()`.

Não acesse mais a API do visualizador depois que `dispose()` for chamado.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
