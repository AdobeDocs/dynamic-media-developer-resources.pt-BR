---
description: Referência da API do JavaScript para o Visualizador de mídia mista.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,Business Practitioner
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

Referência da API do JavaScript para o Visualizador de mídia mista.

` setContainerId( *`containerId`*)`

Define a ID do contêiner DOM (normalmente um DIV) no qual o visualizador é inserido. Não é necessário ter o elemento container criado pelo momento em que esse método é chamado. No entanto, o contêiner deve existir quando `init()` é executado. Ele deve ser chamado antes de `init()`. Esse método é opcional se as informações de configuração do visualizador forem passadas com `config` objeto JSON para o construtor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID do contêiner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
