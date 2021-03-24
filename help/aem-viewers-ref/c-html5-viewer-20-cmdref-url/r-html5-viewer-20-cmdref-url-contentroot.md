---
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
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

