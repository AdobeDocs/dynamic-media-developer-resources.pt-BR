---
description: Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.
solution: Experience Manager
title: dispor
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c4bcccdc-6f23-4213-a1d1-03c5c62ba484
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# dispor{#dispose}

Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.

`dispose()`

Dispõe essa instância do visualizador, liberando todos os recursos usados pela lógica do visualizador e excluindo todos os objetos e componentes internos criados pelo visualizador em tempo de execução.

O código da página da Web também deve excluir a variável da instância do visualizador para remover completamente o visualizador da memória do navegador da Web.

Se o código da página da Web tiver registrado ouvintes de eventos diretamente nos componentes do SDK do visualizador usados pelo visualizador ou referências externas armazenadas nesses componentes, esses ouvintes deverão ser explicitamente cancelados pelo código da página da Web, e essas referências de componentes externos deverão ser excluídas antes de chamar `dispose()`.

Não acesse mais a API do visualizador depois de `dispose()` é chamado.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
