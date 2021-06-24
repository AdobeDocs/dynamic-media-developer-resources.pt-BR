---
description: Referência da API do JavaScript para o Flyout Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o Flyout Viewer.

`init()`

Inicia a inicialização do Flyout Viewer. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento do contêiner ainda não fizer parte do layout da página da Web (por exemplo, pode ser oculto usando o estilo `display:none` atribuído a ele), o visualizador suspende o processo de inicialização até o momento em que a página da Web traz o elemento do contêiner de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Esse método deve ser chamado somente uma vez durante o ciclo de vida do visualizador, as chamadas resultantes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência para a instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
