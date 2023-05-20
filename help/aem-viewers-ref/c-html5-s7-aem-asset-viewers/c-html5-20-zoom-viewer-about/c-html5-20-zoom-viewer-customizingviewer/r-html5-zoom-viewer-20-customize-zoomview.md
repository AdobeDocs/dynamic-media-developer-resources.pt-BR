---
title: Exibição de zoom
description: A visualização principal consiste na imagem com zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Exibição de zoom{#zoom-view}

A visualização principal consiste na imagem com zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo no formato hexadecimal da janela principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>O cursor exibido sobre a visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para tornar a exibição principal transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Nos sistemas de desktop, o componente suporta `cursortype` seletor de atributo que pode ser aplicado ao `.s7zoomview` classe. Ele controla o tipo de cursor com base no estado do componente e na ação do usuário. As seguintes `cursortype` Os valores de são compatíveis:

* `default`

   Exibido quando a imagem não é ampliada devido a uma pequena resolução de imagem, configurações de componente ou ambas.

* `zoomin`

   Exibido quando é possível ampliar a imagem.

* `reset`

   Exibida quando a imagem está no nível de zoom máximo e pode ser redefinida para seu estado inicial.

* `drag`

   Exibido quando o usuário expande a imagem que está no estado ampliado.

* `slide`

   Exibido quando o usuário executa a troca de imagem passando um dedo horizontal ou um toque.
