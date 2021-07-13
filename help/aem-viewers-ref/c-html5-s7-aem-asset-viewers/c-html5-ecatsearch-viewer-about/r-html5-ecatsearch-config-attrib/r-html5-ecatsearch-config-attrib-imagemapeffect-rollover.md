---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Especifica quando exibir o painel de informações. </p> <p>Se definido como <span class="codeph"> 1</span>, o painel de informações é exibido quando o mouse entra na área do mapa de imagem (caso o mapa de imagem tenha atributo <span class="codeph"> rolover_key</span> não vazio). </p> <p>Se definido como <span class="codeph"> 0</span> painel de informações for acionado ao clicar no mapa de imagem (se o mapa de imagem tiver um <span class="codeph"> rolover_key</span> não vazio e <span class="codeph"> href</span> atributos vazios). </p> <p> Ignorado em dispositivos de toque, incluindo sistemas de desktop habilitados para toque, e é automaticamente definido como <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-ccfedc2da28f412a86d03f390db92b4b}

Opcional.

## Padrão {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Exemplo {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
