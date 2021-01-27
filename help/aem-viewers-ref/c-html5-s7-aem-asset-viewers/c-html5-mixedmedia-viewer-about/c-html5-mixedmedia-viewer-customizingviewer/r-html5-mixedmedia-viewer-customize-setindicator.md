---
description: Indicador de definição é uma série de pontos renderizados sobre as amostras principais quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.
seo-description: Indicador de definição é uma série de pontos renderizados sobre as amostras principais quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.
seo-title: Definir indicador
solution: Experience Manager
title: Definir indicador
topic: Dynamic Media
uuid: e62fac7c-28b6-40bf-83cc-8bcfbaa0dfa3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Definir indicador{#set-indicator}

Indicador de definição é uma série de pontos renderizados sobre as amostras principais quando um visualizador é usado em um dispositivo de toque. Os pontos ajudam os usuários a navegar pelas páginas de miniaturas quando os botões de rolagem não estão disponíveis.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS do indicador de conjunto**

A aparência do container indicador definido é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo no formato hexadecimal do indicador de conjunto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o indicador de configuração com um fundo branco:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

A aparência de um ponto indicador de conjunto individual é controlada com o seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do ponto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ponto indicador definido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p>Margem esquerda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p>Margem superior em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita  </span> </p> </td> 
   <td colname="col2"> <p>Margem direita em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Margem inferior em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda  </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Definir ponto indicador suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de miniaturas. Especificamente, `state="selected"` corresponde à página atual das miniaturas, `state="unselected"` corresponde ao estado de ponto padrão.

Exemplo - para configurar o ponto indicador definido como 15 x 15 pixels, com dois pixels de margem horizontal, cinco pixels de margem superior, uma margem inferior de pixel, doze pixels de raio, #D5D3D3 de cor padrão e #939393 de cor ativa:

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

