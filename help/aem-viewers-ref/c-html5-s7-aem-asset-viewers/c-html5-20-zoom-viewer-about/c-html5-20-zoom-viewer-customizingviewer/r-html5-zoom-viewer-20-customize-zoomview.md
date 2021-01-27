---
description: A visualização principal consiste na imagem com zoom.
seo-description: A visualização principal consiste na imagem com zoom.
seo-title: Visualização de zoom
solution: Experience Manager
title: Visualização de zoom
topic: Dynamic Media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Visualização de zoom{#zoom-view}

A visualização principal consiste na imagem com zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursor exibido sobre a visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Em sistemas desktop, o componente suporta o seletor de atributos `cursortype` que pode ser aplicado à classe `.s7zoomview`. Ele controla o tipo do cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` são suportados:

* `default`

   Exibido quando a imagem não tem zoom devido a uma pequena resolução de imagem, configurações de componente ou ambos.

* `zoomin`

   Exibido quando a imagem pode ser ampliada.

* `reset`

   Exibida quando a imagem está no nível máximo de zoom e pode ser redefinida para seu estado inicial.

* `drag`

   Exibido quando o usuário desloca a imagem que está no estado ampliado.

* `slide`

   Exibido quando o usuário executa a troca de imagem fazendo um deslize horizontal ou um movimento.

