---
description: Use os seguintes comandos para formatação avançada de texto.
solution: Experience Manager
title: Formatação de texto avançada
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
TQID: 'https://experienceleague.adobe.com/ZTUWB5N6T-I3DnokCqX--dj9g-807-D9Fv8l20opVkg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# Formatação de texto avançada{#advanced-text-formatting}

Use os seguintes comandos para formatação avançada de texto.

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>Subscrito sem alteração de tamanho de fonte. </p> </td> 
   <td> <p>Posição em meio pontos; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>Sobrescrito sem alteração de tamanho de fonte. </p> </td> 
   <td> <p>Posição em meio pontos; o padrão é 6. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span> </span> </td> 
   <td> <p>Desativar/ativar no tamanho de fonte especificado. </p> </td> 
   <td> <p>Tamanho da fonte em meio pontos, acima do qual aplicar kerning; 0 para desativar kerning; o padrão é 1 para kerning de todos os tamanhos de fonte acima de ½ ponto. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningóptico </span> </td> 
   <td> <p>Selecione kerning óptico. </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>Selecione o kerning métrico. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifique o espaçamento entre caracteres. </p> </td> 
   <td> <p>Trimestres-pontos positivos ou negativos; o padrão é 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>Modifique o espaçamento entre caracteres. </p> </td> 
   <td> <p>Twips positivo ou negativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>Escala de caracteres horizontal. </p> </td> 
   <td> <p>Porcentagem positiva ou negativa; o padrão é 100. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>Escala de caracteres vertical. </p> </td> 
   <td> <p>Porcentagem positiva ou negativa; o padrão é 100; extensão do Dynamic Media. </p> <p> <span class="codeph"> \charscaley </span> também dimensiona o espaçamento entre linhas quando aplicado com <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> sempre preserva o espaçamento entre linhas independentemente da quantidade de dimensionamento de caracteres verticais. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>Selecione fluxo de caracteres da esquerda para a direita. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>Selecione fluxo de caracteres da direita para a esquerda. </p> </td> 
   <td> <p> <span class="codeph"> texto= somente </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ajuste de texto <span class="varname"> N </span> </span> </td> 
   <td> <p>Habilita o ajuste de cópia e define o maior tamanho de fonte permitido. </p> </td> 
   <td> <p>Tamanho da fonte em meio pontos; somente <span class="codeph"> textPs= </span>; extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Máximo de linhas de ajuste de cópia (limitação suave). </p> </td> 
   <td> <p>0 para nenhuma limitação de linha; <span class="codeph"> textPs= </span> somente; extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>Máximo de linhas de ajuste de cópia (truncamento). </p> </td> 
   <td> <p> <span class="codeph"> textPs= somente </span>; extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \linedir <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientação do caractere. </p> </td> 
   <td> <p> <span class="codeph"> textPs= somente </span>; ignorado para fontes não romanas; ignorado quando <span class="codeph"> \stextflow1 </span> não está em vigor. </p> <p>0 vertical (padrão). </p> <p>1 girado 90 graus no sentido horário. </p> </td> 
  </tr> 
 </tbody> 
</table>
