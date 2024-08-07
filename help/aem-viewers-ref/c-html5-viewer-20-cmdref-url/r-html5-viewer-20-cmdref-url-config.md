---
title: config
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# config{#config}

Parâmetro comum a todos os visualizadores.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Catálogo/ID da configuração do visualizador. </p> <p> Especifica uma entrada de catálogo de imagens que contém as propriedades de configuração do visualizador no catálogo <span class="codeph">::UserData </span>. Quando este comando está presente, o visualizador envia um comando <span class="codeph"> req=userdata </span> para <span class="codeph"> configId </span> ao servidor e extrai propriedades da resposta. As propriedades são usadas para inicializar o visualizador. Se a cadeia de caracteres de URL especificar as mesmas propriedades, elas substituirão os valores de <span class="codeph"> catalog::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Todos os comandos do visualizador que podem ser especificados em `catalog::UserData` esperam ele mesmo `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` e `config`.

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

Nenhum.

## Exemplo 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Um catálogo de imagens chamado 2020 contém a entrada `preset-oct`. O campo `catalog::UserData` desta entrada de catálogo inclui os seguintes dados:

```
style=customStyle.css
```

Carregue o visualizador com o seguinte comando:

```
config=2020/preset-oct
```

Este exemplo é equivalente ao seguinte comando especificado explicitamente no URL:

```
style=customStyle.css
```

## Exemplo 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

Um catálogo de imagens chamado 2019 contém a entrada `spin-oct`. O campo `catalog::UserData` desta entrada de catálogo inclui os seguintes dados:

```
zoomStep=3 
maxZoom=200
```

Carregue o visualizador com o seguinte comando:

```
config=2019/spin-oct
```

Este exemplo é equivalente ao seguinte comando especificado explicitamente no URL:

```
zoomStep=3&maxZoom=200
```

## Exemplo 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

Uma predefinição do visualizador chamada `Shoppable_Banner` inclui os seguintes dados:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Carregue o visualizador com o seguinte comando:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Este exemplo é equivalente aos seguintes comandos especificados explicitamente no URL:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Exemplo 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

Uma predefinição do visualizador chamada `Shoppable_Video_Dark` contém os seguintes dados:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Carregue o visualizador com o seguinte comando:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Este exemplo é equivalente aos seguintes comandos especificados explicitamente no URL:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Exemplo 5 {#section-19b988551d1d492a9079948e0b04b38f}

Uma predefinição do visualizador chamada `Carousel_Dotted_light` os seguintes dados:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Carregue o visualizador com o seguinte comando:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Este exemplo é equivalente aos seguintes comandos especificados explicitamente no URL:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
