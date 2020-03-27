---
description: Referência da API JavaScript para o visualizador de rotação.
seo-description: Referência da API JavaScript para o visualizador de rotação.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Referência da API JavaScript para o visualizador de rotação.

`init()`

Start a inicialização do Visualizador de rotação. Nesse momento, o elemento de container deve ser criado para que o código do visualizador possa encontrá-lo por sua ID. `DOM`

Se o elemento container ainda não fizer parte do layout da página da Web (por exemplo, pode estar oculto usando o `display:none` estilo atribuído a ele), o visualizador suspenderá seu processo de inicialização até o momento em que a página da Web trazer o elemento container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Chame este método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

