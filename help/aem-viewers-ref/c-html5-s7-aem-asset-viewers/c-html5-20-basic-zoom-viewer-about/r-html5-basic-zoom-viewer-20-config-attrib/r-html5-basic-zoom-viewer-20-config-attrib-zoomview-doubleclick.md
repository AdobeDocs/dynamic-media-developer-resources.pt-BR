---
description: nulo
seo-description: nulo
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 676a13b5-4634-4233-8059-6effed6e2b5d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clicar/tocar em duplo para aplicar zoom. Definir como <span class="codeph"> nenhum </span> desativa o zoom de clique/toque em duplo. Se definido para <span class="codeph"> ampliar, </span> clicar no zoom da imagem é ampliado em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. A configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, redefinir será aplicado se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` sobre computadores de secretária; `zoomReset` em dispositivos de toque.

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
