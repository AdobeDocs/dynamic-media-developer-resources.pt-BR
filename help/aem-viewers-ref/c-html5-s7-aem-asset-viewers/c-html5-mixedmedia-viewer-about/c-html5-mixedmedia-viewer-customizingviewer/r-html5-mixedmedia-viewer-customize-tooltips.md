---
title: Dicas de ferramentas
description: Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bbf8e8f0-eb1c-49fa-a501-4c7ed7827595
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Dicas de ferramentas{#tooltips}

Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

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
   <td colname="col2"> <p> Raio da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda </span> </p> </td> 
   <td colname="col2"> <p> Cor da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes </span> </p> </td> 
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
>Caso os estilos de dica de ferramenta sejam personalizados na página da Web de incorporação, todas as propriedades precisam conter `!IMPORTANT` regra. Essa regra não é necessária se as dicas de ferramentas forem personalizadas no arquivo CSS do visualizador.

Exemplo - Para configurar dicas de ferramentas com uma borda cinza com raio de canto de 3 px, plano de fundo preto e texto branco gravado com Arial®, tamanho de 11 pixels:

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
