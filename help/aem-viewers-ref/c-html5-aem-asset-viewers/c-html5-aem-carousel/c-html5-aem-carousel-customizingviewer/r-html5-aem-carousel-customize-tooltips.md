---
description: Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas que são exibidas ao passar o mouse.
solution: Experience Manager
title: Dicas de ferramentas
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: b4604528-93f6-440c-b676-7b4c89fff6c8
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Dicas de ferramentas{#tooltips}

Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas que são exibidas ao passar o mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência das dicas de ferramenta é controlada com o seguinte seletor de classe CSS:

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda  </span> </p> </td> 
   <td colname="col2"> <p> Cor da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Caso os estilos de dica de ferramenta sejam personalizados na página da Web de incorporação, todas as propriedades precisam conter a regra `!IMPORTANT`. Isso não é necessário se as dicas de ferramentas forem personalizadas no arquivo CSS do visualizador.

Exemplo - para configurar dicas de ferramentas com uma borda cinza com um raio de canto de 3 pixels, plano de fundo preto e texto branco em Arial, tamanho de 11 pixels:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
