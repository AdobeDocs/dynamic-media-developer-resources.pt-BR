---
description: Opções para cortar automaticamente imagens com base em cores.
seo-description: Opções para cortar automaticamente imagens com base em cores.
seo-title: AutoColorCropOptions
solution: Experience Manager
title: AutoColorCropOptions
topic: Dynamic Media Image Production System API
uuid: 632ae721-7b39-4cd1-a1c6-1a3554167a4e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---


# AutoColorCropOptions{#autocolorcropoptions}

Opções para cortar automaticamente imagens com base em cores.

Sintaxe

## Parâmetros {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> canto</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Escolha de Canto de Corte Automático. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerância</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:duplo</span> </td> 
   <td colname="col3">Especificação de correspondência de cor. Usa: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 para corresponder as cores exatamente. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 para ativar a maioria das diferenças de cor. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

