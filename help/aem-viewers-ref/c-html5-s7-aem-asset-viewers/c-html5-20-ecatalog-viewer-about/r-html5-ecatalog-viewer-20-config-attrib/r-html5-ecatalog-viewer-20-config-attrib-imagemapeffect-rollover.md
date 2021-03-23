---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
uuid: 92bd8ced-1c41-4147-96fa-5f77bdd6a316
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

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

`0`

## Exemplo {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
