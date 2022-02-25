---
title: Exibição de zoom
description: A exibição principal consiste na imagem com zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Exibição de zoom{#zoom-view}

A exibição principal consiste na imagem com zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>O cursor é exibido sobre a exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Em sistemas de desktop, o componente suporta o `cursortype` seletor de atributos que pode ser aplicado ao `.s7zoomview` controla o tipo de cursor com base no estado do componente e na ação do usuário. O seguinte `cursortype` são compatíveis:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valor </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Exibida quando a imagem não é ampliável devido a uma pequena resolução de imagem, configurações de componente ou ambos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando a imagem puder ser ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> redefinir </span> </p> </td> 
   <td colname="col2"> <p>Exibida quando a imagem está no nível máximo de zoom e pode ser redefinida para o estado inicial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrastar </span> </p> </td> 
   <td colname="col2"> <p>Exibido quando um usuário expande a imagem que está no estado ampliado. </p> </td> 
  </tr> 
 </tbody> 
</table>
