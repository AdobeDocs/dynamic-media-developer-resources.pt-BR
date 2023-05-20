---
title: Definir indicador
description: Definir indicador é uma série de pontos renderizados na parte inferior do visualizador. Ela mostra a posição atual no conjunto.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Definir indicador{#set-indicator}

Definir indicador é uma série de pontos renderizados na parte inferior do visualizador. Ela mostra a posição atual no conjunto.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS do indicador de definição**

A aparência do contêiner do indicador de definição é controlada com o seguinte seletor de classe CSS:

```
.s7carouselviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo em formato hexadecimal do indicador de definição. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Definir indicador suporta o seletor de atributo de modo, que você pode usar para aplicar diferentes estilos para modos de operação pontilhados e numéricos. Em especial, `mode="numeric"` corresponde ao modo de operação numérico; `mode="dotted"` corresponde ao estado de ponto padrão.

Por exemplo, suponha que você queira configurar um indicador de definição com um fundo branco:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

A aparência de um ponto indicador de definição individual é controlada com o seletor de classe CSS. Ela se aplica a itens nos modos de operação pontilhados e numéricos.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do ponto indicador de definição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do ponto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p>Margem esquerda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p>Margem superior em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita </span> </p> </td> 
   <td colname="col2"> <p>Margem direita em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem inferior </span> </p> </td> 
   <td colname="col2"> <p>Margem inferior em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo em formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-alinhamento </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento vertical do índice do banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p>Altura do texto para o índice do banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Definir itens indicadores para suportar o `state` seletor de atributos, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Em especial, `state="selected"` corresponde ao elemento atual no conjunto; `state="unselected"` corresponde ao estado de item padrão.

Por exemplo, suponha que você queira configurar um indicador definido em modo pontilhado para sistemas desktop. Você deseja que ele seja posicionado 20 pixels da parte inferior do visualizador. E você deseja que os pontos não selecionados sejam pretos com 50% de transparência, 15 x 15 pixels com sete pixels de vértices arredondados. Os pontos selecionados são pretos com 90% de transparência, 18 x 18 pixels com nove pixels de cantos arredondados. O espaçamento entre pontos é de cinco pixels.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
