---
description: nulo
seo-description: nulo
seo-title: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
topic: Dynamic media
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`número`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre|nunca|limite</span> </p> </td> 
   <td colname="col2"> <p> Ative, limite ou desative a otimização para dispositivos em que <span class="codeph"> devicePixelRatio</span> é maior que <span class="codeph"> 1</span>, ou seja, dispositivos com uma tela de alta densidade, como o iPhone4 e dispositivos semelhantes. Se ativo, o componente limita o tamanho da solicitação de imagem IS como se o dispositivo tivesse apenas uma proporção de pixel de <span class="codeph"> 1</span> e, portanto, reduzindo a largura de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> número</span></span> </p> </td> 
   <td colname="col2"> <p> Se estiver usando a configuração de <span class="codeph"> limite</span> , o componente ativará a alta densidade de pixels apenas até o limite especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
