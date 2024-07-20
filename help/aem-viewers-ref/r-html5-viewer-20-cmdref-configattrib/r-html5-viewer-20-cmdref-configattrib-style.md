---
title: estilo
description: estilo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# estilo{#style}

Você pode aplicar o seguinte comando a partir da string de consulta e da configuração do URL. O comando aplicado na cadeia de caracteres de consulta do URL sempre tem prioridade sobre o mesmo comando presente na configuração.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Local de CSS relativo ou absoluto. </p> <p>Especifica o local do arquivo CSS personalizado. Se o <span class="codeph"><span class="varname"> cssPath</span></span> for relativo, ele será resolvido em relação ao local da página de HTML do visualizador e ao valor do parâmetro <span class="codeph"> contentUrl=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Todas as referências de ativos no arquivo CSS são resolvidas em relação ao local do arquivo CSS, não ao local da página do HTML de chamada.

## Propriedades {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Opcional.

## Padrão {#section-79a827f7a3bb4f36b3d72c309155059e}

Nenhum.

## Exemplos {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
