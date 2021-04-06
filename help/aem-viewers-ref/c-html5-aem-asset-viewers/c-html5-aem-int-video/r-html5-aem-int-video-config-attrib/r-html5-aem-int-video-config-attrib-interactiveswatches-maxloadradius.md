---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Atributo de configuração para o Visualizador de vídeo interativo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> todas as amostras são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p>Quando definido como <span class="codeph"> 0</span>, apenas as amostras visíveis são carregadas. </p> <p>Defina como <span class="codeph"><span class="varname"> pré-carregamento</span></span> para definir quantas linhas/colunas invisíveis ao redor da área visível são pré-carregadas. </p> </td> 
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
