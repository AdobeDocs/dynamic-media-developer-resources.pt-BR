---
title: init
description: Referência da API do JavaScript para o Visualizador de imagem interativa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 675031ab-21bb-49a5-abbc-eca8d2619e49
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de imagem interativa.

`init()`

Inicia a inicialização do Visualizador de Imagens Interativas. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento do contêiner ainda não fizer parte do layout da página da Web - por exemplo, ele pode ser oculto usando o estilo `display:none` atribuído a ele - o visualizador suspende seu processo de inicialização. Isso ocorre até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência para a instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
