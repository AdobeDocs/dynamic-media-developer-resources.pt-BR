---
title: init
description: Referência da API do JavaScript para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9e83b773-c059-45c6-a249-ef0ed2799a05
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de vídeo.

`init()`

Inicia a inicialização do Visualizador de Vídeo. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web (por exemplo, talvez ele esteja oculto usando o estilo `display:none`), o visualizador suspenderá seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando esse processo acontece, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
