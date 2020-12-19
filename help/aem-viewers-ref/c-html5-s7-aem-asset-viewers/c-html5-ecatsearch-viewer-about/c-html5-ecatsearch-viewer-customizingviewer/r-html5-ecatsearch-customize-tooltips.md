---
description: Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.
seo-description: Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.
seo-title: Dicas de ferramentas
solution: Experience Manager
title: Dicas de ferramentas
topic: Dynamic media
uuid: 2cbf8a22-5d0e-46e3-b6e3-29739439558b
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# Dicas de ferramentas{#tooltips}

Em sistemas de desktop, alguns elementos da interface do usuário, como botões, têm dicas de ferramentas exibidas ao passar o mouse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> raio da borda  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor da borda  </span> </p> </td> 
   <td colname="col2"> <p> Cor da borda do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Caso os estilos de dica de ferramenta sejam personalizados na página da Web de incorporação, todas as propriedades devem conter a regra `!IMPORTANT`. Isso não é necessário se as dicas de ferramentas forem personalizadas no arquivo CSS do visualizador.

Exemplo - para configurar dicas de ferramentas que tenham uma borda cinza com raio de canto de 3px, plano de fundo preto e texto branco gravados com Arial, tamanho de 11 pixels:

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

