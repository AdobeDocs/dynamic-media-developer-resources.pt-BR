---
description: nulo
seo-description: nulo
seo-title: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
topic: Dynamic media
uuid: c62302b0-d034-49d4-b5a8-1a77a46fe889
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoom|Reset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clicar/tocar em duplo para aplicar zoom. A configuração para <span class="codeph"> none </span> desativa o zoom de clique/toque em duplo. Se definido para <span class="codeph"> zoom </span> clicando no zoom da imagem em uma etapa de zoom; CTRL+Clique diminui o zoom em uma etapa. Definir para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou acima do limite especificado, caso contrário o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Padrão {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] sobre computadores de secretária;  [!DNL `zoomReset`] em dispositivos de toque.

## Exemplo {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
