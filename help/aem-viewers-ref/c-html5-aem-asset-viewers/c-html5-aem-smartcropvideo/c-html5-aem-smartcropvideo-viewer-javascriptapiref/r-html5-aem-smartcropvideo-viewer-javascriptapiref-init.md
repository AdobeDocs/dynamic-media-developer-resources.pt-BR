---
title: init
description: Referência da API do JavaScript para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de vídeo de recorte inteligente.

`init()`

Inicia a inicialização do Visualizador de Corte inteligente de vídeo. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web - por exemplo, talvez ele esteja oculto usando o estilo `display:none` atribuído a ele - o visualizador suspende seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação acontece, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
