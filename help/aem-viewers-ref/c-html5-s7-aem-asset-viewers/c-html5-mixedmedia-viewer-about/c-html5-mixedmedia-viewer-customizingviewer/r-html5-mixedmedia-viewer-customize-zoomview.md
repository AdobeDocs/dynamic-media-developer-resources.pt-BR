---
description: No modo de zoom contínuo, a visualização principal consiste na imagem com zoom quando o ativo atual é uma única imagem.
solution: Experience Manager
title: Exibição de zoom
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Developer,Business Practitioner
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Exibição de zoom{#zoom-view}

No modo de zoom contínuo, a visualização principal consiste na imagem com zoom quando o ativo atual é uma única imagem.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo em formato hexadecimal da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursor exibido sobre a exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição de zoom transparente.

```
.s7mixedmediaviewer .s7zoomview { 
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
