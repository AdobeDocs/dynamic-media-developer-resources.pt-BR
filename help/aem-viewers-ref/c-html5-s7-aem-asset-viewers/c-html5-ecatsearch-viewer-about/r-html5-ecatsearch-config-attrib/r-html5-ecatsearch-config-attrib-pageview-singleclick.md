---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique único/toque para ações de zoom. Configurar como <span class="codeph"> nenhum </span> desabilita o zoom de clique único/toque. Se estiver definido como <span class="codeph">, o zoom </span> ao clicar na imagem dá zoom de uma só vez; CTRL+Clique dá zoom de uma só vez. Configurar como <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível inicial. Para <span class="codeph"> zoomReset </span>, a redefinição é aplicada se o fator de zoom atual estiver no limite especificado ou além dele, caso contrário o zoom é aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Padrão {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] em computadores desktop; [!DNL `none`] em dispositivos de toque.

## Exemplo {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
