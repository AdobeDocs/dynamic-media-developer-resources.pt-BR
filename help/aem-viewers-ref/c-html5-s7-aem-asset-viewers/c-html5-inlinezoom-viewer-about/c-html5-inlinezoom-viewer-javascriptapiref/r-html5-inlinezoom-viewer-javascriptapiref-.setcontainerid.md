---
description: Referência da API JavaScript para Visualizador de zoom incorporado.
seo-description: Referência da API JavaScript para Visualizador de zoom incorporado.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic Media
uuid: 52f81748-d007-4f42-9057-7947cc02b231
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# setContainerId{#setcontainerid}

Referência da API JavaScript para Visualizador de zoom incorporado.

` setContainerId( *`containerId`*)`

Define a ID do container DOM (normalmente um `DIV`) no qual o visualizador é inserido. Não é necessário ter o elemento de container criado no momento em que esse método é chamado. No entanto, o container deve existir quando `init()` for executado. Ele deve ser chamado antes de `init()`. Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto `config` JSON para o construtor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID do container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

