---
description: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Developer,User
exl-id: 394b79cd-0611-4496-86e3-366a2ffc6ca7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# PageView.enableHD{#pageview-enablehd}

[!DNL `[PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`número`*]`]

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Ative, limite ou desative a otimização para dispositivos em que <span class="codeph"> devicePixelRatio</span> é maior que <span class="codeph"> 1</span>, ou seja, dispositivos com exibição de alta densidade como iPhone4 e dispositivos semelhantes. Se estiver ativo, o componente limita o tamanho da solicitação de imagem IS como se o dispositivo tivesse apenas uma proporção de pixel de <span class="codeph"> 1</span> e, dessa forma, reduz a largura de banda. </p> <p>Consulte o exemplo abaixo </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Se estiver usando a configuração de limite, o componente ativará a alta densidade de pixels somente até o limite especificado. </p> <p>Consulte o exemplo abaixo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-38b878e38caa439bb462d4fa637afdaa}

Opcional.

## Padrão {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## Exemplo {#section-09433488774245d985acef6c0341ece0}

Os resultados a seguir são esperados quando você usa esse atributo de configuração com o visualizador e o tamanho do visualizador é 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se a variável definida for igual a </p> </th> 
   <th colname="col2" class="entry"> <p>Resultado </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> always</span> </p> </td> 
   <td colname="col2"> <p>A densidade de pixels da tela/dispositivo é sempre levada em conta. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Se a densidade de pixels da tela for = 1, a imagem solicitada será 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Se a densidade de pixels da tela for = 1,5, a imagem solicitada será 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Se a densidade de pixels da tela for = 2, a imagem solicitada será 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> never</span> </p> </td> 
   <td colname="col2"> <p>Ele sempre usa uma densidade de pixels de 1 e ignora o recurso de HD do dispositivo. Portanto, a imagem solicitada é sempre 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limite&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Uma densidade de pixels de dispositivo é solicitada e veiculada somente se a imagem resultante estiver abaixo do limite especificado. </p> <p>O número limite se aplica à dimensão largura ou altura. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Se o número limite for 1600 e a densidade de pixels for 1,5, a imagem 1500 x 1500 será veiculada. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Se o número limite for 1600 e a densidade de pixels for 2, a imagem 1000 x 1000 será veiculada porque a imagem 2000 x 2000 excede o limite. </p> </li> 
     </ul> </p> <p><b>Prática</b> recomendada: O número limite precisa funcionar em conjunto com a configuração da empresa para imagem de tamanho máximo. Portanto, defina o número limite como igual à configuração de tamanho máximo da imagem da empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>
