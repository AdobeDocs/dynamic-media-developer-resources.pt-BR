---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aumentar o zoom. Definir para <span class="codeph"> nenhum </span> desativa o zoom de clique único/toque. Se definido como <span class="codeph"> zoom </span> clicando nos zoom da imagem em uma etapa de zoom; CTRL + Clique com o zoom para baixo em uma etapa de zoom. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou além do limite especificado, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Padrão {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` em computadores de secretária;  `none` em dispositivos de toque.

## Exemplo {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
