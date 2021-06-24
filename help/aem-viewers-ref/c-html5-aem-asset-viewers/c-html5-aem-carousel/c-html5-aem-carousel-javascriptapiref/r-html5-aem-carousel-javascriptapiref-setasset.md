---
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Developer,Business Practitioner
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador do carrossel.

` setAsset( *`ativo`*)`

Define o novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nova ID de ativo. </p> <p>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```
