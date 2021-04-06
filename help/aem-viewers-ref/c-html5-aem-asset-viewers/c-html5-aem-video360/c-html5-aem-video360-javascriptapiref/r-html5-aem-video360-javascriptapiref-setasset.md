---
description: Referência da API do JavaScript para o visualizador do Video360.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o visualizador do Video360.

`setAsset(asset)`

Define o novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ativo  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nova ID de ativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```
