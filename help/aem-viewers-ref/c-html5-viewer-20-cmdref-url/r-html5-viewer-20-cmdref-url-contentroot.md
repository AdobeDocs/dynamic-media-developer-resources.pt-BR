---
description: Parâmetro comum a todos os visualizadores.
seo-description: Parâmetro comum a todos os visualizadores.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---


# contentUrl{#contenturl}

Parâmetro comum a todos os visualizadores.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o caminho base para arquivos CSS personalizados, qualquer conteúdo de legenda ou conteúdo de navegação. </p> <p>Se o caminho não tiver um <span class="filepath"> /</span> à esquerda, ele será relativo ao local da página HTML do visualizador. Se o caminho tiver um <span class="filepath"> /</span> à esquerda, ele especificará um caminho absoluto no mesmo servidor. </p> <p> Não afeta o carregamento do arquivo CSS padrão quando um comando de estilo não é especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

