---
title: setAsset
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
TQID: 'https://experienceleague.adobe.com/ybqfHaH3Eu3NRJMpMLCtkglIE0iyywJJz1oBoPkecOQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador do carrossel.

` setAsset( *`ativo`*)`

Define o novo ativo. Você pode chamar este parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador trocará o ativo no tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadeia de caracteres</span>} nova ID do ativo. </p> <p>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador. </p> </td>
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

