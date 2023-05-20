---
title: Dicas de ferramenta
description: Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas que são exibidas ao passar o mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 051bfbed-103e-4fcf-9f01-93f03730397a
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# Dicas de ferramenta{#tooltips}

Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas que são exibidas ao passar o mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência das dicas de ferramentas é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Cor da borda do fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Se os estilos de dica de ferramenta forem personalizados na página da Web de incorporação, todas as propriedades deverão conter a `!IMPORTANT` regra. Essa regra não é necessária se as dicas de ferramentas forem personalizadas no arquivo CSS do visualizador.

Exemplo - Para configurar dicas de ferramentas que tenham uma borda cinza com um raio de canto de três pixels, plano de fundo preto e texto branco em Arial®, 11 pixels:

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
