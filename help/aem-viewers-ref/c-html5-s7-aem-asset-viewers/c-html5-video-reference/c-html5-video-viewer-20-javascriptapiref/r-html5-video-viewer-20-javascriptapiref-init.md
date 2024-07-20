---
title: init
description: Referência da API do JavaScript para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de vídeo.

`init()`

Inicia a inicialização do Visualizador de Vídeo. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web - por exemplo, talvez ele esteja oculto usando o estilo `display:none` atribuído a ele - o visualizador suspende seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação ocorre, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
