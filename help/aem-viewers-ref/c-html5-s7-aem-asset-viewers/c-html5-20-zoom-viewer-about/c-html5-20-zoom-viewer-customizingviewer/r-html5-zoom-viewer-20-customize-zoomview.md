---
description: A exibição principal consiste na imagem com zoom.
solution: Experience Manager
title: Exibição de zoom
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Visualização de zoom{#zoom-view}

A exibição principal consiste na imagem com zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursor exibido sobre a exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Em sistemas de desktop, o componente suporta `cursortype` seletor de atributos que pode ser aplicado à classe `.s7zoomview`. Ele controla o tipo do cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` são suportados:

* `default`

   Exibida quando a imagem não é ampliável devido a uma pequena resolução de imagem, configurações de componente ou ambos.

* `zoomin`

   Exibido quando a imagem puder ser ampliada.

* `reset`

   Exibida quando a imagem está no nível máximo de zoom e pode ser redefinida para o estado inicial.

* `drag`

   Exibido quando o usuário expande a imagem que está no estado ampliado.

* `slide`

   Exibido quando o usuário realiza a troca de imagem fazendo um deslizamento horizontal ou um clique.

