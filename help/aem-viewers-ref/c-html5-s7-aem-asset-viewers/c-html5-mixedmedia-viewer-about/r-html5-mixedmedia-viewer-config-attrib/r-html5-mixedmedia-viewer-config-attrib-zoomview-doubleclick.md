---
description: nulo
seo-description: nulo
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
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

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` sobre computadores de secretária; `zoomReset` em dispositivos de toque.

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
