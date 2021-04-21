---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de ações de clique/toque único para aumentar o zoom. Definir para <span class="codeph"> nenhum </span> desativa o zoom de clique único/toque. Se definido como <span class="codeph"> zoom </span> clicando nos zoom da imagem em uma etapa de zoom; CTRL + Clique com o zoom para baixo em uma etapa de zoom. Configurar para <span class="codeph"> redefinir </span> faz com que um único clique na imagem redefina o zoom para o nível inicial de rotação. Para <span class="codeph"> zoomReset </span>, a redefinição será aplicada se o fator de zoom atual estiver dentro ou além do limite especificado, caso contrário, o zoom será aplicado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` em computadores de secretária;  `none` em dispositivos de toque.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
