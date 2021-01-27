---
description: Parâmetro comum a todos os visualizadores.
seo-description: Parâmetro comum a todos os visualizadores.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic Media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
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
   <td colname="col2"> <p>Caminho raiz relativo ou absoluto do Servidor de imagens. </p> <p> Especifica um caminho relativo ou absoluto para o Serviço de imagens, a partir do qual o visualizador recupera imagens. Se o caminho não tiver um <span class="filepath"> /</span> à esquerda, ele será relativo ao local da página HTML do visualizador. Se o caminho tiver um <span class="filepath"> /</span> à esquerda, ele especificará um caminho absoluto no mesmo servidor. </p> <p> Use apenas um caminho absoluto caso o módulo Compartilhamento por email esteja ativado no visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. Não é necessário para o uso padrão do SaaS (software como serviço).

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

