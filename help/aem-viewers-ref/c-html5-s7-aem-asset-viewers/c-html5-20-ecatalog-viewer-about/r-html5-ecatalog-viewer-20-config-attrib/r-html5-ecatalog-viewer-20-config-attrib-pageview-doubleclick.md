---
description: nulo
seo-description: nulo
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: ac4fb532-f554-4831-b341-7f8d6ef3a1c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clicar/tocar em duplo para aplicar zoom. Definir como <span class="codeph"> nenhum </span> desativa o zoom de clique/toque em duplo. Se definido para <span class="codeph"> ampliar, </span> clicar no zoom da imagem é ampliado em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. A configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, redefinir será aplicado se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Padrão {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` sobre computadores de secretária; `zoomReset` em dispositivos de toque.

## Example {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
