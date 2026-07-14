---
description: Referência da API do JavaScript para o eCatalog Viewer.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
TQID: 'https://experienceleague.adobe.com/NOaYrj9ntatmLob6D2xY-MxJEGBMGkZYHoo04HXMeOY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# setParams{#setparams}

Referência da API do JavaScript para o eCatalog Viewer.

[!DNL ` setParams( *`parâmetros`*)`]

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, ele representa pares name=value separados por [!DNL `&`]. Assim como em uma sequência de consulta, os nomes e os valores são codificados por porcentagem usando UTF8. Antes de chamar [!DNL `init()`], esse parâmetro deve ser chamado.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto JSON [!DNL `config`] para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parâmetros</span> </span> </p> </td> 
   <td colname="col2"> <p> Pares de parâmetros <span class="codeph"> {string}</span> name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
