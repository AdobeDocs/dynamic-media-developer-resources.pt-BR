---
title: Dicas de ferramenta
description: Em sistemas desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 706b27a1-99e8-4596-8bd1-af4455501e29
TQID: 'https://experienceleague.adobe.com/XCh49qhOtYcrwZ0jYYFwLoPcG-6o2-5TCQK3iOT4JJU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# Dicas de ferramenta{#tooltips}

Em sistemas desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.

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
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda </span> </p> </td> 
   <td colname="col2"> <p> Cor da borda do fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Se os estilos de dica de ferramenta forem personalizados na página da Web incorporada, todas as propriedades deverão conter a regra `!IMPORTANT`. Essa regra não é necessária se as dicas de ferramentas forem personalizadas no arquivo CSS do visualizador.

Exemplo - Para configurar dicas de ferramentas com uma borda cinza com raio de canto de três pixels, plano de fundo preto e texto branco escrito com Arial®, tamanho de 11 pixels:

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
