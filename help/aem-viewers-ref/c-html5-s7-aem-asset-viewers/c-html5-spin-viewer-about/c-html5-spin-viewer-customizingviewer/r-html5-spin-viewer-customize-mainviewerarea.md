---
description: A área de visualização principal é a área ocupada pela imagem de rotação. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.
seo-description: A área de visualização principal é a área ocupada pela imagem de rotação. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.
seo-title: Área do visualizador principal
solution: Experience Manager
title: Área do visualizador principal
uuid: 8395386b-4039-4a47-8d31-a341813c2647
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# Área do visualizador principal{#main-viewer-area}

A área de visualização principal é a área ocupada pela imagem de rotação. Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7spinviewer
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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um visualizador com um plano de fundo branco ( `#FFFFFF`) e tornar seu tamanho 512 x 288 pixels.

```
.s7spinviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

