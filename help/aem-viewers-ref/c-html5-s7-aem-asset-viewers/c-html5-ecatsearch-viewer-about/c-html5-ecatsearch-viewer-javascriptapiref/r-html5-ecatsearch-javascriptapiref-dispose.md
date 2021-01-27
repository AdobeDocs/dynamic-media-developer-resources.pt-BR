---
description: Referência da API JavaScript para o eCatalog Viewer.
seo-description: Referência da API JavaScript para o eCatalog Viewer.
seo-title: dispor
solution: Experience Manager
title: dispor
topic: Dynamic Media
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# dispor{#dispose}

Referência da API JavaScript para o eCatalog Viewer.

[!DNL `dispose()`]

Descarta essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador em tempo de execução.

O código da página da Web também deve excluir a variável de instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de evento diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas a esses componentes, esses ouvintes deverão ser explicitamente não registrados pelo código da página da Web, e essas referências de componentes externos deverão ser excluídas antes de chamar [!DNL `dispose()`].

Não acesse mais a API do visualizador depois que [!DNL `dispose()`] for chamado.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

