---
title: Barra de controle secundária
description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última página e um Indicador de página quando disponibilizados no CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2354c3a0-2df7-4a18-aac1-fac158a9b659
TQID: 'https://experienceleague.adobe.com/aT-NQikSvfT9khT6idoN9HcN6oDJBzJv6zoo0G8wg1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# Barra de controle secundária{#secondary-control-bar}

A barra de controle secundária é a área retangular que contém os botões Primeira e Última página e um Indicador de página quando disponibilizados no CSS.

Por padrão, é exibido apenas em celulares e está posicionado na parte inferior do visualizador. Leva sempre toda a largura disponível do visualizador. É possível alterar a cor, a altura e a posição vertical por CSS, em relação ao contêiner do visualizador.

A aparência da barra de controle secundária é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição na parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo da barra de controle secundária. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de controle secundária cinza com 72 pixels de altura e posicionada na parte inferior do contêiner do visualizador.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
