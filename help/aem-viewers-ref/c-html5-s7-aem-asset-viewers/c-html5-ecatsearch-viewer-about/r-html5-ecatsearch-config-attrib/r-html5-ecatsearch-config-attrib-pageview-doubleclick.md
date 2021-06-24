---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Developer,Business Practitioner
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo clique/toque para aplicar zoom às ações. Definir para <span class="codeph"> nenhum </span> desativa o zoom de duplo clique/toque. Se definido como <span class="codeph"> zoom </span> clicando nos zoom da imagem em uma etapa de zoom; CTRL + Clique com o zoom para baixo em uma etapa de zoom. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível de zoom inicial. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou além do limite especificado, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Padrão {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] em computadores de secretária;  [!DNL `zoomReset`] em dispositivos de toque.

## Exemplo {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
