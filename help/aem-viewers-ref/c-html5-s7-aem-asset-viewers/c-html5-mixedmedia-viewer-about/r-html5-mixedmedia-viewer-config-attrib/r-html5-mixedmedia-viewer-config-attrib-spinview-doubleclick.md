---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de duplo clique/toque para girar ações. Configurar para <span class="codeph"> nenhum </span> desativa o duplo clique/toque em rotação. Se definido como <span class="codeph"> zoom </span>, clicar na imagem gira em uma etapa de rotação; CTRL+Clique gira uma etapa de rotação. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o giro para o nível inicial de rotação. Para <span class="codeph"> zoomReset </span>, a redefinição é aplicada se o fator de rotação atual estiver no limite especificado ou além dele, caso contrário a rotação é aplicada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` em computadores de secretária;  `zoomReset` em dispositivos de toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
