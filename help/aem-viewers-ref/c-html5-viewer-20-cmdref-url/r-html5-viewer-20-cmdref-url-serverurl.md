---
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
title: serverUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# serverUrl{#serverurl}

Parâmetro comum a todos os visualizadores.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Caminho raiz relativo ou absoluto do Serviço de imagem. </p> <p> Especifica um caminho relativo ou absoluto para o Serviço de imagem, de onde o visualizador recupera imagens. Se o caminho não tiver um <span class="filepath"> /</span> à esquerda, ele será relativo ao local da página HTML do visualizador. Se o caminho tiver um <span class="filepath"> /</span> à esquerda, ele especificará um caminho absoluto no mesmo servidor. </p> <p> Use apenas um caminho absoluto caso o módulo Compartilhamento de email esteja ativado no visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. Não é necessário para o uso padrão do SaaS (software como um serviço).

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Exemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
