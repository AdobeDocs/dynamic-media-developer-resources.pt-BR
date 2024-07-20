---
title: init
description: Referência da API do JavaScript para inicialização do Visualizador de imagem suspensa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Visualizador de submenu.

`init()`

Inicia a inicialização do Visualizador de Submenu. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web — por exemplo, ele poderá ser ocultado usando o estilo `display:none` atribuído a ele — o visualizador suspende seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Esse método deve ser chamado apenas uma vez durante o ciclo de vida do visualizador. As chamadas resultantes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
