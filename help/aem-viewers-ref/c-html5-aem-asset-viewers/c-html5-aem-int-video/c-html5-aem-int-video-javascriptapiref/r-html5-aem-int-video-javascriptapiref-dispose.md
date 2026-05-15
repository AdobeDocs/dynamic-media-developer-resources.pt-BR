---
title: descartar
description: Referência da API do JavaScript para o visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 55418b97-3d18-4c1d-b0e3-aefd71f46616
TQID: 'https://experienceleague.adobe.com/dTZbs-HDOLZndZTnasH-zSi8Q70vYFv-sfqMCJP3gPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 0%

---

# descartar{#dispose}

Referência da API do JavaScript para o visualizador de vídeo interativo.

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
