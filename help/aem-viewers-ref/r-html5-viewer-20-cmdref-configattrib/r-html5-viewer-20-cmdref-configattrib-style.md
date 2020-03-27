---
description: nulo
seo-description: nulo
seo-title: estilo
solution: Experience Manager
title: estilo
topic: Dynamic media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# estilo{#style}

Você pode aplicar o seguinte comando da string do query URL e da configuração. O comando aplicado na string do query URL sempre tem precedência sobre o mesmo comando presente na configuração.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span></span> </p> </td> 
   <td colname="col2"> <p> Local CSS relativo ou absoluto. </p> <p>Especifica o local do arquivo CSS personalizado. Se o <span class="codeph"><span class="varname"> cssPath</span></span> for relativo, ele será resolvido em relação ao local da página HTML do visualizador e ao valor do parâmetro <span class="codeph"> contentUrl=</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

Todas as referências de ativos no arquivo CSS são resolvidas em relação ao local do arquivo CSS, não ao local da página HTML chamadora.

## Propriedades {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Opcional.

## Padrão {#section-79a827f7a3bb4f36b3d72c309155059e}

Nenhum.

## Exemplos {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
