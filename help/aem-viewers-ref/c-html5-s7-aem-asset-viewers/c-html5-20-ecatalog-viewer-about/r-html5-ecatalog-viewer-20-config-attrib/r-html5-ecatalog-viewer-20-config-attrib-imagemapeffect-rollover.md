---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>Especifica quando exibir o painel de informações. </p> <p>Se definida como <span class="codeph"> 1</span>, o painel de informações é exibido quando o mouse entra na área do mapa de imagem (caso o mapa de imagem não esteja vazio, <span class="codeph"> rollover_key</span> atributo). </p> <p>Se definida como <span class="codeph"> 0</span> o painel informações é acionado quando o mapa de imagem é selecionado (se o mapa de imagem tiver um painel não vazio) <span class="codeph"> rollover_key</span> e vazio <span class="codeph"> href</span> atributos). </p> <p> Ignorado em dispositivos de toque, incluindo sistemas de desktop habilitados para toque, e é automaticamente definido como <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-ccfedc2da28f412a86d03f390db92b4b}

Opcional.

## Padrão {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Exemplo {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
