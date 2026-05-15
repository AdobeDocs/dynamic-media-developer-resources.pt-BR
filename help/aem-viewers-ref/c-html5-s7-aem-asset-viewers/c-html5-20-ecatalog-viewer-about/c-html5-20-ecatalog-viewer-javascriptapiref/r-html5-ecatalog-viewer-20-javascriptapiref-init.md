---
title: init
description: Referência da API do JavaScript para o eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
TQID: 'https://experienceleague.adobe.com/T33OIUSYMKmrpLGhp8Sia-p8RwyKjEnIMP4Dfp-JgF4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# init{#init}

Referência da API do JavaScript para o eCatalog Viewer.

`init()`

Inicia a inicialização do Visualizador de eCatalog. Nesse momento, o elemento DOM do contêiner de tempo deve ser criado para que o código do visualizador possa localizá-lo pela ID.

Se o elemento de contêiner ainda não fizer parte do layout da página da Web - por exemplo, talvez ele esteja oculto usando o estilo `display:none` atribuído a ele - o visualizador suspende seu processo de inicialização. Isso é feito até o momento em que a página da Web traz o elemento de contêiner de volta ao layout. Quando essa ação acontece, o carregamento do visualizador é retomado automaticamente.

Chame esse método apenas uma vez durante o ciclo de vida do visualizador; as chamadas subsequentes são ignoradas.

## Parâmetros {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nenhum.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Uma referência à instância do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
