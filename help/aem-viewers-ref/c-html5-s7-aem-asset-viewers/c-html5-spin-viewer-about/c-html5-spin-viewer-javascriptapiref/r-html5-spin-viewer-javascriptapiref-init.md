---
title: init
description: Referência da API JavaScript para o Visualizador de rotação.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# init{#init}

Referência da API JavaScript para o Visualizador de rotação.

`init()`

Inicia a inicialização do Visualizador de rotação. Nesse momento, o container `DOM` O elemento deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web - por exemplo, ele pode estar oculto usando `display:none` style - o visualizador suspende o processo de inicialização. Ela fica suspensa até o momento em que a página da Web traz o elemento de contêiner de volta ao layout, momento em que o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
