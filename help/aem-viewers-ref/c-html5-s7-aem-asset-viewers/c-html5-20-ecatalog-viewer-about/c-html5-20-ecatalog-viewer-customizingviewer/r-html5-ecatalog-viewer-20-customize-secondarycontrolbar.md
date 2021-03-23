---
description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última Página e um Indicador de Página quando disponibilizado em CSS.
seo-description: A barra de controle secundária é a área retangular que contém os botões Primeira e Última Página e um Indicador de Página quando disponibilizado em CSS.
seo-title: Barra de controle secundária
solution: Experience Manager
title: Barra de controle secundária
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Barra de controle secundária{#secondary-control-bar}

A barra de controle secundária é a área retangular que contém os botões Primeira e Última Página e um Indicador de Página quando disponibilizado em CSS.

Por padrão, ele é exibido somente em telefones celulares e está localizado na parte inferior do visualizador. Sempre leva toda a largura disponível do visualizador. É possível alterar sua cor, altura e posição vertical por CSS, em relação ao contêiner do visualizador.

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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posicione a partir da parte inferior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da barra de controle secundária. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de controle secundária cinza com 72 pixels de altura e que esteja posicionada na parte inferior do contêiner do visualizador.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

