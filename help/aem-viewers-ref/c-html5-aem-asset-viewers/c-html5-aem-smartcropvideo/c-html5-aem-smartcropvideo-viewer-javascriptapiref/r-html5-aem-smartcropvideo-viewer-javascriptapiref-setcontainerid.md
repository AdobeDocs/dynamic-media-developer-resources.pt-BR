---
title: setContainerId
description: Referência da API do JavaScript para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 1c7a7494-e872-4e78-9518-ea30af46303c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

Referência da API do JavaScript para o Visualizador de vídeo de recorte inteligente.

` setContainerId( *`containerId`*)`

Define a ID do contêiner DOM (normalmente um `DIV`) no qual o visualizador está inserido. Não é necessário criar o elemento de contêiner quando esse método for chamado. No entanto, o contêiner deve existir quando `init()` é executado. Este parâmetro é chamado antes de `init()`. Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto JSON `config` para o construtor.

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
