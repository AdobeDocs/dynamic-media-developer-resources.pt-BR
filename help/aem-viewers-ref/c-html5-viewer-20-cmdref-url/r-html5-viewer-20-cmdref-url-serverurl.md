---
title: serverUrl
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
TQID: 'https://experienceleague.adobe.com/SbAeHSjxnw-69wsu92UeoEeGLlk3Ykpechs65I-k5EY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# serverUrl{#serverurl}

Parâmetro comum a todos os visualizadores.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Caminho raiz relativo ou absoluto do Servidor de imagens. </p> <p> Especifica um caminho relativo ou absoluto para o Servidor de imagens, de onde o visualizador recupera imagens. Se o caminho não tiver um <span class="filepath"> /</span> à esquerda, ele será relativo ao local da página do visualizador do HTML. Se o caminho tiver um <span class="filepath"> /</span> à esquerda, ele especifica um caminho absoluto no mesmo servidor. </p> <p> Use apenas um caminho absoluto caso o módulo de compartilhamento de email esteja habilitado no visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. Não é necessário para o uso padrão de SaaS (software como serviço).

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Exemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
