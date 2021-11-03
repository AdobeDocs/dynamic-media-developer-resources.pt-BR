---
title: setContainerId
description: Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.

` setContainerId( *`containerId`*)`

Define a ID do contêiner DOM (normalmente um `DIV`) em que o visualizador é inserido. Não é necessário ter o elemento container criado pelo momento em que esse método é chamado. No entanto, o contêiner deve existir quando `init()` é executado. Este parâmetro é chamado antes de `init()`. Esse método é opcional se as informações de configuração do visualizador forem passadas com `config` Objeto JSON para o construtor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID do contêiner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
