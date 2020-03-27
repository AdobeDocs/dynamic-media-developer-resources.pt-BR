---
description: nulo
seo-description: nulo
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aplicar zoom. Definir como <span class="codeph"> nenhum </span> desativa o zoom de clique único/toque. Se definido para <span class="codeph"> ampliar, </span> clicar no zoom da imagem é ampliado em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. A configuração para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, redefinir será aplicado se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Padrão {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] sobre computadores de secretária; [!DNL `none`] em dispositivos de toque.

## Example {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]