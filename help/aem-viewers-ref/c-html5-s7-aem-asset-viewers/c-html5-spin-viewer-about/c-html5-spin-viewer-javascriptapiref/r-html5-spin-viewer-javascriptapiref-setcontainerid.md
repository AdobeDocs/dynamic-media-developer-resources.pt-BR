---
title: setContainerId
description: Referência da API do JavaScript para o Visualizador de rotação.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5859800f-7d01-4c32-a67f-211578d5c50b
TQID: 'https://experienceleague.adobe.com/SSLbiTPttNGL2BwPqZUwPasc7oWmvBUForQmOFmDJGc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# setContainerId{#setcontainerid}

Referência da API do JavaScript para o Visualizador de rotação.

` setContainerId( *`containerId`*)`

Define a ID do contêiner DOM (normalmente um DIV) no qual o visualizador é inserido. Não é necessário criar o elemento de contêiner quando esse método for chamado. No entanto, o contêiner deve existir quando `init()` é executado. Ele deve ser chamado antes de `init()`.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto JSON `config` para o construtor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID do container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
