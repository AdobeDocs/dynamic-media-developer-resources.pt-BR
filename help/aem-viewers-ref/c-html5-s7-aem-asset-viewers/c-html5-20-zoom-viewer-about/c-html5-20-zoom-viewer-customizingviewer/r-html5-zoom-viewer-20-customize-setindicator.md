---
title: Definir indicador
description: Definir indicador é uma série de pontos renderizados sobre amostras quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
TQID: 'https://experienceleague.adobe.com/y4QBgUjYMAh5-FlbA32Zgg0Peve1FcO-qhDxc0Ypv4M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 0%

---

# Definir indicador{#set-indicator}

Definir indicador é uma série de pontos renderizados sobre amostras quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS do indicador de definição**

A aparência do contêiner do indicador de definição é controlada com o seguinte seletor de classe CSS:

```
.s7zoomviewer .s7setindicator
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
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

A aparência de um ponto indicador de definição individual é controlada com o seletor de classe CSS:

`.s7zoomviewer .s7setindicator .s7dot`

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

Exemplo - Para criar um ponto indicador definido para ser de 15 x 15 pixels, com margem horizontal de 2 pixels, margem superior de 5 pixels, margem inferior de 1 pixel, raio de 12 pixels, cor padrão #D5D3D3 e cor ativa #939393:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

