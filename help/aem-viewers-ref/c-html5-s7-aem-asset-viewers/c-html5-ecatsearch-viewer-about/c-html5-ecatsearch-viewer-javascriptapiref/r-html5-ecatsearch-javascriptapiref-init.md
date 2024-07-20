---
title: init
description: Referência da API do JavaScript para o eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o eCatalog Viewer.

[!DNL `init()`]

Inicia a inicialização do Visualizador de eCatalog. Nesse momento, o elemento DOM do contêiner deve ser criado para que o código do visualizador possa encontrá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web (por exemplo, talvez ele esteja oculto usando o estilo [!DNL `display:none`] atribuído a ele), o visualizador suspenderá seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando esse evento ocorre, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
