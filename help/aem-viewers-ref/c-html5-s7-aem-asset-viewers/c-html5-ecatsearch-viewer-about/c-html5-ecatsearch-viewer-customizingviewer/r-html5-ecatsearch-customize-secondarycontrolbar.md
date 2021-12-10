---
title: Barra de controle secundária
description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última Página e um Indicador de Página quando disponibilizado em CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Barra de controle secundária{#secondary-control-bar}

A barra de controle secundária é a área retangular que contém os botões Primeira e Última Página e um Indicador de Página quando disponibilizado em CSS.

Por padrão, ele é exibido somente em telefones celulares, na parte inferior do visualizador. Sempre leva toda a largura disponível do visualizador. É possível alterar a cor, a altura e a posição vertical por CSS, em relação ao contêiner do visualizador.

A aparência da barra de controle secundária é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

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
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posicione a partir da parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da barra de controle secundária. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de controle secundária cinza com 72 pixels de altura e que esteja posicionada na parte inferior do contêiner do visualizador.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
