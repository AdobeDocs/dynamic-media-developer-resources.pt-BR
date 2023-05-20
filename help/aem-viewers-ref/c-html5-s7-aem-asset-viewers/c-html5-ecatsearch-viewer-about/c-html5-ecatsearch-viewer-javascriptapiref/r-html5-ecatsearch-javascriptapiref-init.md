---
description: Referência da API JavaScript para o eCatalog Viewer.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# init{#init}

Referência da API JavaScript para o eCatalog Viewer.

[!DNL `init()`]

Inicia a inicialização do Visualizador de eCatalog. Nesse momento, o elemento DOM do contêiner de tempo deve ser criado para que o código do visualizador possa localizá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web (por exemplo, ele pode estar oculto usando [!DNL `display:none`] estilo atribuído a ele), o visualizador suspende o processo de inicialização até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando isso acontece, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
