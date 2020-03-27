---
description: Referência da API JavaScript para o visualizador do Video360.
seo-description: Referência da API JavaScript para o visualizador do Video360.
seo-title: dispor
solution: Experience Manager
title: dispor
topic: Dynamic media
uuid: bdecadb1-4e77-43d5-9da5-80e5101efb36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# dispor{#dispose}

Referência da API JavaScript para o visualizador do Video360.

`dispose()`

Descarta essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador em tempo de execução.

O código da página da Web também deve excluir a variável de instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de evento diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas a esses componentes, esses ouvintes deverão ser explicitamente não registrados pelo código da página da Web, e essas referências de componentes externos deverão ser excluídas antes da chamada `dispose()`.

Não acesse mais a API do visualizador depois de `dispose()` ser chamada.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

