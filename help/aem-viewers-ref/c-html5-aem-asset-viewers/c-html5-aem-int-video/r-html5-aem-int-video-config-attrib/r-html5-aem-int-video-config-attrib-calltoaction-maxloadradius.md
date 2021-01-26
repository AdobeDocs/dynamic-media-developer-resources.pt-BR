---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: CallToAction.maxloadradius
solution: Experience Manager
title: CallToAction.maxloadradius
topic: Dynamic Media
uuid: ec5a4b0d-1dae-456f-a9da-91541cfba1a7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---


# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Atributo de configuração para o Visualizador de vídeo interativo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> todas as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p>Quando definido como <span class="codeph"> 0</span> apenas miniaturas visíveis são carregadas. </p> <p>Defina como <span class="codeph"><span class="varname"> preloadnbr</span></span> para definir quantas linhas/colunas invisíveis ao redor da área visível são pré-carregadas. </p> </td> 
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

