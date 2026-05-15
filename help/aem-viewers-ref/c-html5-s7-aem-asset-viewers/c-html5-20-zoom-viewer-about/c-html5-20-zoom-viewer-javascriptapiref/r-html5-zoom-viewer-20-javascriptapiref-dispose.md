---
title: descartar
description: Referência da API do JavaScript para o Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c796943e-8ea8-4a97-a1ff-09676204150a
TQID: 'https://experienceleague.adobe.com/Fi7inW4o2cQ5r3518sL7n8GWCJZeVf94Za4-2unBzRE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# descartar{#dispose}

Referência da API do JavaScript para o Zoom Viewer.

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
