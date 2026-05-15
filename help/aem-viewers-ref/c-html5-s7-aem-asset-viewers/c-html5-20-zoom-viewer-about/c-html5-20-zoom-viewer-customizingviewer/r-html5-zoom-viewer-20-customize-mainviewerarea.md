---
title: Área do visualizador principal
description: A área de exibição principal é a área ocupada pela imagem de zoom e pelas amostras. Normalmente, ele é configurado para se ajustar à tela do dispositivo disponível quando nenhum tamanho é especificado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
TQID: 'https://experienceleague.adobe.com/mAfXI6eLoLmVR7yI6EvUjlVjQrQ8J86ikUZGa5rRN4E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 0%

---

# Área do visualizador principal{#main-viewer-area}

A área de exibição principal é a área ocupada pela imagem de zoom e pelas amostras. Normalmente, ele é configurado para se ajustar à tela do dispositivo disponível quando nenhum tamanho é especificado.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Ao trabalhar no modo incorporado (quando um tamanho explícito é fornecido para a área do visualizador principal), o visualizador diminui automaticamente a altura de sua área principal pela altura do componente Amostras que está trabalhando com a única imagem e, portanto, as amostras não são necessárias.

**Propriedades CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo em formato hexadecimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um visualizador com um plano de fundo branco ( `#FFFFFF`) e definir seu tamanho como 512 x 288 pixels.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
