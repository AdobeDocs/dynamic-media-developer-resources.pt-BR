---
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
title: dispor
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Developer,Business Practitioner
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# dispor{#dispose}

Referência da API do JavaScript para o Visualizador do carrossel.

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
