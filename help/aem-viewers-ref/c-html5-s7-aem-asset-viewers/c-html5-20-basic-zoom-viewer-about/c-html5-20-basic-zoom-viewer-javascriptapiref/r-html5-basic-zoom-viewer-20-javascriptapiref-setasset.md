---
title: setAsset
description: Referência da API do JavaScript para o Visualizador de zoom básico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de zoom básico.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadeia de caracteres</span>} nova ID do ativo, com modificadores IS opcionais anexados após "?" </p> <p> As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são compatíveis com esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define o novo ativo. Você pode chamar este parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador trocará o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Modificador de nitidez adicionado a todas as imagens do conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```
