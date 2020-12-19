---
description: Referência da API JavaScript para o eCatalog Viewer.
seo-description: Referência da API JavaScript para o eCatalog Viewer.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# init{#init}

Referência da API JavaScript para o eCatalog Viewer.

[!DNL `init()`]

Start a inicialização do eCatalog Viewer. Nesse momento, o elemento DOM do container deve ser criado para que o código do visualizador possa encontrá-lo por sua ID.

Se o elemento container ainda não fizer parte do layout da página da Web (por exemplo, pode estar oculto usando o estilo [!DNL `display:none`] atribuído a ele), o visualizador suspenderá seu processo de inicialização até o momento em que a página da Web trazer o elemento container de volta ao layout. Quando isso ocorre, o carregamento do visualizador é retomado automaticamente.

Chamar este método apenas uma vez durante o ciclo de vida do visualizador; chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

