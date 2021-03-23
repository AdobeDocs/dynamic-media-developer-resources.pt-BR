---
description: A área de visualização principal é ocupada pelo vídeo. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.
seo-description: A área de visualização principal é ocupada pelo vídeo. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.
seo-title: Área do visualizador principal
solution: Experience Manager
title: Área do visualizador principal
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Área do visualizador principal{#main-viewer-area}

A área de visualização principal é ocupada pelo vídeo. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

O seguinte seletor de classe CSS controla a aparência da área de visualização:

```
.s7videoviewer 
```

## Propriedades CSS da área do visualizador principal {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um visualizador de vídeo com um fundo branco (#FFFFF) e tornar seu tamanho 512 x 288 pixels:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

