---
title: InterativeSwatches.maxloadradius
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
TQID: 'https://experienceleague.adobe.com/BhsXOdgu2cCLX9hJEzn6PgW-aRjAZUybM4c891T7gZs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 0%

---

# InterativeSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Atributo de configuração para o Visualizador de vídeo interativo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento do carregamento prévio do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> todas as amostras são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p>Quando definido como <span class="codeph"> 0</span>, somente as amostras visíveis são carregadas. </p> <p>Defina como <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir quantas linhas/colunas invisíveis em torno da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
