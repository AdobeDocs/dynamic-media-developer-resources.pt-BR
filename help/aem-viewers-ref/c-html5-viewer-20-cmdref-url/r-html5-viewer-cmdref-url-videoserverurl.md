---
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

Parâmetro comum a todos os visualizadores.

>[!NOTE]
>
>Este comando não se aplica ao Visualizador de imagem de vídeo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> O caminho raiz do servidor de vídeo. Se nenhum domínio for especificado, o domínio do qual a página é disponibilizada será aplicado. A resolução de caminho URI padrão se aplica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. Não é necessário para o software padrão como uso de serviço.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
