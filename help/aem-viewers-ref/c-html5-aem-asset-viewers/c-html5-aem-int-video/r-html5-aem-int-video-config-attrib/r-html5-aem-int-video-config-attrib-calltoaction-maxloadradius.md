---
title: CallToAction.maxloadradius
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Atributo de configuração para o Visualizador de vídeo interativo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento do carregamento prévio do componente. </p> <p>Quando definido como <span class="codeph"> -1</span>, todas as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p>Quando definido como <span class="codeph"> 0</span>, somente as miniaturas visíveis são carregadas. </p> <p>Defina como <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir quantas linhas/colunas invisíveis em torno da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`-1`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
