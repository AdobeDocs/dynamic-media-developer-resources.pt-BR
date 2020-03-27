---
description: Referência da API JavaScript para o visualizador de rotação.
seo-description: Referência da API JavaScript para o visualizador de rotação.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 6ed57f8f-5a5e-4dfa-9ab5-0f724603a0bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

Referência da API JavaScript para o visualizador de rotação.

` setContainerId( *`containerId`*)`

Define a ID do container DOM (normalmente um DIV) no qual o visualizador é inserido. Não é necessário ter o elemento de container criado no momento em que esse método é chamado. No entanto, o container deve existir quando `init()` é executado. Deve ser chamado antes `init()`.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto `config` JSON para o construtor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID do container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

