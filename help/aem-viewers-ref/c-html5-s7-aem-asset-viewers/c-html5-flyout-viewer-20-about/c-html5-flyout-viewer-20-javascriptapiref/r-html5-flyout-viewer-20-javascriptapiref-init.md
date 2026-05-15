---
title: init
description: Referência da API do JavaScript para inicialização do Visualizador de imagem suspensa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
TQID: 'https://experienceleague.adobe.com/vavSoeUebo8YrntPoPKm3why-Jbzrh4p6v8Eqmgsv1I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
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
