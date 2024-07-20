---
title: Definir indicador
description: Definir indicador é uma série de pontos renderizados sobre as principais amostras quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Definir indicador{#set-indicator}

Definir indicador é uma série de pontos renderizados sobre as principais amostras quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS do indicador de definição**

A aparência do contêiner do indicador de definição é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo em formato hexadecimal do indicador de definição. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para criar um indicador de definição com um plano de fundo branco:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

A aparência de um ponto indicador de definição individual é controlada com o seletor de classe CSS:

`.s7mixedmediaviewer .s7setindicator .s7dot`

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
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Definir ponto indicador dá suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Especificamente, `state="selected"` corresponde à página atual de miniaturas, `state="unselected"` corresponde ao estado de ponto padrão.

Exemplo - Para criar um ponto indicador de definição com 15 x 15 pixels, com uma margem horizontal de dois pixels, margem superior de cinco pixels, margem inferior de um pixel, raio de 12 pixels, cor padrão #D5D3D3 e cor ativa #939393:

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
