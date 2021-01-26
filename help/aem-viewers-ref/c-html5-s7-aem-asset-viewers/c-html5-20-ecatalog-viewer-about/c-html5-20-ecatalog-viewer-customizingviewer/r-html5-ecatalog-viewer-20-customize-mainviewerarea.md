---
description: A área de visualização principal é a área ocupada pela imagem do catálogo. Geralmente, ele é definido para ajustar a tela do dispositivo disponível quando nenhum tamanho é especificado.
seo-description: A área de visualização principal é a área ocupada pela imagem do catálogo. Geralmente, ele é definido para ajustar a tela do dispositivo disponível quando nenhum tamanho é especificado.
seo-title: Área do visualizador principal
solution: Experience Manager
title: Área do visualizador principal
topic: Dynamic Media
uuid: e337058e-1b51-4bc8-bfdb-95c1500db16a
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Área do visualizador principal{#main-viewer-area}

A área de visualização principal é a área ocupada pela imagem do catálogo. Geralmente, ele é definido para ajustar a tela do dispositivo disponível quando nenhum tamanho é especificado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>A largura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um visualizador com um fundo branco ( `#FFFFFF`) e tornar seu tamanho 512 x 288 pixels.

```
.s7ecatalogviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

