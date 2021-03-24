---
description: Use os seguintes comandos para formatação de texto avançada.
solution: Experience Manager
title: Formatação de texto avançada
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Formatação de texto avançada{#advanced-text-formatting}

Use os seguintes comandos para formatação de texto avançada.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrição </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Subscript sem alteração do tamanho da fonte. </p> </td> 
   <td> <p>Posição em meio ponto; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Sobrescrito sem alteração do tamanho da fonte. </p> </td> 
   <td> <p>Posição em meio ponto; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Desative/ative no tamanho de fonte especificado. </p> </td> 
   <td> <p>Tamanho da fonte em meio ponto, acima do qual aplicar ajuste de espaço; 0 para desativar o ajuste do espaço; o padrão é 1 para kerning de todos os tamanhos de fonte em meio ponto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningótico  </span> </td> 
   <td> <p>Selecione ajuste do espaço óptico. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> somente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>Selecione o ajuste do espaço da métrica. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expandir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificar o espaçamento entre caracteres. </p> </td> 
   <td> <p>Valores trimestrais positivos ou negativos; o padrão é 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Modificar o espaçamento entre caracteres. </p> </td> 
   <td> <p>Twips positivos ou negativos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Escala horizontal de caracteres. </p> </td> 
   <td> <p>Percentagem positiva ou negativa; o padrão é 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Escala vertical de caracteres. </p> </td> 
   <td> <p>Percentagem positiva ou negativa; o padrão é 100; Extensão do Dynamic Media. </p> <p> <span class="codeph"> \charscale  </span> também dimensiona o espaçamento entre linhas quando aplicado com  <span class="codeph"> texto=  </span>. <span class="codeph"> textPs=  </span> sempre preserva o espaçamento entre linhas, independentemente da quantidade de dimensionamento vertical de caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \traço  </span> </td> 
   <td> <p>Selecione o fluxo de caracteres da esquerda para a direita. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>Selecione o fluxo de caracteres da direita para a esquerda. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Habilite o ajuste da cópia e defina o maior tamanho de fonte permitido. </p> </td> 
   <td> <p>Tamanho da fonte em meio ponto; <span class="codeph"> apenas textPs= </span>; Extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Máximo de linhas de ajuste da cópia (limite suave). </p> </td> 
   <td> <p>0 sem limitação de linha; <span class="codeph"> apenas textPs= </span>; Extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Máximo de linhas de ajuste da cópia (truncamento). </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; Extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientação dos caracteres. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorado para fontes não romanas; ignorado quando  <span class="codeph"> \stextflow1 não  </span> está em vigor. </p> <p>0 vertical (padrão). </p> <p>1 girado 90 graus no sentido horário. </p> </td> 
  </tr> 
 </tbody> 
</table>

