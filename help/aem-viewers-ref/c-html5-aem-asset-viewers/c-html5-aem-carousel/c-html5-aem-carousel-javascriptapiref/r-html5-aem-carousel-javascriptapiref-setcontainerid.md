---
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

Referência da API do JavaScript para o Visualizador do carrossel.

` setContainerId( *`containerId`*)`

Define a ID do contêiner DOM (normalmente um `DIV`) no qual o visualizador é inserido. Não é necessário ter o elemento container criado pelo momento em que esse método é chamado. No entanto, o contêiner deve existir quando `init()` é executado. Ele deve ser chamado antes de `init()`.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto JSON `config` para o construtor.

## Parâmetro {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID do contêiner. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
