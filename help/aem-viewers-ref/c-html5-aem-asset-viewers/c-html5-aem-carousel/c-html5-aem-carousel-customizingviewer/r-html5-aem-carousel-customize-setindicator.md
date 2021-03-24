---
description: O indicador Set é uma série de pontos renderizados na parte inferior do visualizador. Mostra a posição atual no conjunto.
solution: Experience Manager
title: Definir indicador
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Definir indicador{#set-indicator}

O indicador Set é uma série de pontos renderizados na parte inferior do visualizador. Mostra a posição atual no conjunto.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS do indicador de conjunto**

A aparência do contêiner indicador definido é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo em formato hexadecimal do indicador definido. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O indicador Set suporta o seletor de atributo mode, que pode ser usado para aplicar estilos diferentes para modos de operação pontilhados e numéricos. Em particular, `mode="numeric"` corresponde ao modo de operação numérico; `mode="dotted"` corresponde ao estado de ponto padrão.

Exemplo - para configurar o indicador de configuração com um fundo branco:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

A aparência de um ponto indicador de conjunto individual é controlada com o seletor de classe CSS. Aplica-se a itens em modos de operação pontilhados e numéricos.

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo em formato hexadecimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento vertical  </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento vertical do índice do banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha  </span> </p> </td> 
   <td colname="col2"> <p>Altura do texto para o índice do banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Os itens do indicador definido oferecem suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Em particular, `state="selected"` corresponde ao elemento atual no conjunto; `state="unselected"` corresponde ao estado padrão do item.

Exemplo - para configurar o indicador de configuração no modo pontilhado para que os sistemas de desktop sejam posicionados 20 pixels a partir da parte inferior do visualizador. Os pontos não selecionados são pretos com 50% de transparência, 15 x 15 pixels com 7 pixels de cantos arredondados. Os pontos selecionados são pretos com 90% de transparência, 18 x 18 pixels com 9 pixels de cantos arredondados. O espaçamento entre pontos é de 5 pixels.

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

