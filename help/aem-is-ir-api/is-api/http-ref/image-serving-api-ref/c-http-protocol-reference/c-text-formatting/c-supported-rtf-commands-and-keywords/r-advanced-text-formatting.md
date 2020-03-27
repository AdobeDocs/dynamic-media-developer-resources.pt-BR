---
description: Use os seguintes comandos para a formatação de texto avançada.
seo-description: Use os seguintes comandos para a formatação de texto avançada.
seo-title: Formatação de texto avançada
solution: Experience Manager
title: Formatação de texto avançada
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Formatação de texto avançada{#advanced-text-formatting}

Use os seguintes comandos para a formatação de texto avançada.

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span></span> </td> 
   <td> <p>Subscrito sem alteração do tamanho da fonte. </p> </td> 
   <td> <p>Posição em semispontos; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span></span> </td> 
   <td> <p>Sobrescrito sem alteração no tamanho da fonte. </p> </td> 
   <td> <p>Posição em semispontos; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span></span> </td> 
   <td> <p>Desabilitar/habilitar no tamanho de fonte especificado. </p> </td> 
   <td> <p>Tamanho da fonte em meio ponto, acima do qual aplicar ajuste de espaço; 0 para desativar o ajuste de espaço; o padrão é 1 para ajustar o espaço de todos os tamanhos de fonte em ½ ponto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningótico </span> </td> 
   <td> <p>Selecione ajuste de espaço óptico. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Selecione o ajuste de espaço da métrica. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expent <span class="varname"> N </span></span> </td> 
   <td> <p>Modifique o espaçamento entre caracteres. </p> </td> 
   <td> <p>Valores trimestrais positivos ou negativos; o padrão é 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span></span> </td> 
   <td> <p>Modifique o espaçamento entre caracteres. </p> </td> 
   <td> <p>Twips positivos ou negativos. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescalex <span class="varname"> N </span></span> </td> 
   <td> <p>Escala horizontal de caracteres. </p> </td> 
   <td> <p>Percentagem positiva ou negativa; o padrão é 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charescaley <span class="varname"> N </span></span> </td> 
   <td> <p>Escala vertical de caracteres. </p> </td> 
   <td> <p>Percentagem positiva ou negativa; o padrão é 100; Extensão Scene7. </p> <p> <span class="codeph"> \charescaley </span> também dimensiona o espaçamento entre linhas quando aplicado com <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> sempre preserva o espaçamento entre linhas, independentemente da quantidade de escala vertical de caracteres. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Selecione o fluxo de caracteres da esquerda para a direita. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Selecione o fluxo de caracteres da direita para a esquerda. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span></span> </td> 
   <td> <p>Ative o ajuste de cópia e defina o tamanho de fonte mais alto permitido. </p> </td> 
   <td> <p>Tamanho da fonte em meio ponto; somente <span class="codeph"> textPs= </span> ; Extensão Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copy fitlines <span class="varname"> N </span></span> </td> 
   <td> <p>Máximo de linhas de ajuste de cópia (limite suave). </p> </td> 
   <td> <p>0 sem limitação de linha; somente <span class="codeph"> textPs= </span> ; Extensão Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copy fitmaxlines <span class="varname"> N </span></span> </td> 
   <td> <p>Máximo de linhas de ajuste de cópia (truncamento). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; Extensão Scene7. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span></span> </td> 
   <td> <p>Orientação do caractere. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only; ignorado para fontes não romanas; ignorado quando <span class="codeph"> \stextflow1 </span> não está em vigor. </p> <p>0 vertical (padrão). </p> <p>1 girado 90 graus no sentido horário. </p> </td> 
  </tr> 
 </tbody> 
</table>

