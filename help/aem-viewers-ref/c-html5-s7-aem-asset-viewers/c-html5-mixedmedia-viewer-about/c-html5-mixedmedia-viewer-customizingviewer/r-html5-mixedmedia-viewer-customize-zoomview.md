---
description: No modo de zoom contínuo, a visualização principal consiste na imagem com zoom quando o ativo atual é uma única imagem.
seo-description: No modo de zoom contínuo, a visualização principal consiste na imagem com zoom quando o ativo atual é uma única imagem.
seo-title: Visualização de zoom
solution: Experience Manager
title: Visualização de zoom
topic: Dynamic Media
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# Visualização de zoom{#zoom-view}

No modo de zoom contínuo, a visualização principal consiste na imagem com zoom quando o ativo atual é uma única imagem.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7zoomview
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

Exemplo - para tornar a visualização de zoom transparente.

```
.s7mixedmediaviewer .s7zoomview { 
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

