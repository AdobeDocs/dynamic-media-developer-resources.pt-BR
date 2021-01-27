---
description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última página e um Indicador de página quando disponibilizado no CSS.
seo-description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última página e um Indicador de página quando disponibilizado no CSS.
seo-title: Barra de controle secundária
solution: Experience Manager
title: Barra de controle secundária
topic: Dynamic Media
uuid: 38217d2a-8668-46e1-9df1-f29c1c7e0798
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# Barra de controle secundária{#secondary-control-bar}

A barra de controle secundária é a área retangular que contém os botões Primeira e Última página e um Indicador de página quando disponibilizado no CSS.

Por padrão, ele é exibido somente em telefones celulares e está localizado na parte inferior do visualizador. Ele sempre leva a largura total do visualizador disponível. É possível alterar sua cor, altura e posição vertical por CSS, em relação ao container do visualizador.

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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo da barra de controle secundária. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de controle secundária cinza com 72 pixels de altura e posicionada na parte inferior do container do visualizador.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

