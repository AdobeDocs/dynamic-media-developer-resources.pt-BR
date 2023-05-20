---
description: Referência da API JavaScript para o Visualizador de vídeo.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API JavaScript para o Visualizador de vídeo.

[!DNL ` setAsset( *`ativo`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nova ID do ativo ou conjunto de imagens explícitas com modificadores opcionais do Servidor de imagens anexados após <span class="codeph"> ? </span>. </p> <p> Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define um novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de [!DNL `init()`]. Se for chamado depois de [!DNL `init()`], o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência única a um conjunto de imagens definido em um catálogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Conjunto de imagens explícito, com páginas pré-combinadas:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Conjunto de imagens explícito, com imagens de página individuais:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificador de nitidez adicionado a todas as imagens do conjunto:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
