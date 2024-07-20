---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre|nunca|limite</span> </p> </td> 
   <td colname="col2"> <p> Habilite, limite ou desabilite a otimização para dispositivos em que <span class="codeph"> devicePixelRatio</span> é maior que <span class="codeph"> 1</span>, ou seja, dispositivos com exibição de alta densidade como iPhone4 e dispositivos semelhantes. Se estiver ativo, o componente limitará o tamanho da solicitação de imagem IS como se o dispositivo só tivesse uma proporção de pixels de <span class="codeph"> 1</span>, reduzindo assim a largura de banda. </p> <p>Veja o exemplo abaixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> número</span> </span> </p> </td> 
   <td colname="col2"> <p> Se estiver usando a configuração de limite, o componente permitirá a densidade de pixels alta somente até o limite especificado. </p> <p>Veja o exemplo abaixo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

Os resultados esperados são os seguintes quando você usa esse atributo de configuração com o visualizador e o tamanho do visualizador é 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se a variável do conjunto for igual a </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre</span> </p> </td> 
   <td colname="col2"> <p>A densidade de pixels da tela/dispositivo é sempre considerada.</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Se a densidade de pixels da tela = 1, a imagem solicitada será 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Se a densidade de pixels da tela = 1,5, a imagem solicitada é 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Se a densidade de pixels da tela = 2, a imagem solicitada é 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nunca</span> </p> </td> 
   <td colname="col2"> <p>Ele sempre usa uma densidade de pixels de 1 e ignora o recurso de alta definição do dispositivo. Portanto, a imagem solicitada é sempre 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limite&lt;número&gt;</span> </p> </td> 
   <td colname="col2"> <p>Uma densidade de pixels de dispositivo é solicitada e veiculada somente se a imagem resultante estiver abaixo do limite especificado. </p> <p>O número de limite se aplica às dimensões largura ou altura. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Se o número limite for 1600 e a densidade de pixels for 1,5, a imagem de 1500 x 1500 será fornecida. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Se o número limite for 1600 e a densidade de pixels for 2, a imagem 1000 x 1000 será fornecida porque a imagem 2000 x 2000 excede o limite. </p> </li> 
     </ul> </p> <p> <b>Prática recomendada</b>: o número limite deve funcionar com a configuração da empresa para a imagem de tamanho máximo. Portanto, defina o número limite para ser igual à configuração de tamanho máximo de imagem da empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>
