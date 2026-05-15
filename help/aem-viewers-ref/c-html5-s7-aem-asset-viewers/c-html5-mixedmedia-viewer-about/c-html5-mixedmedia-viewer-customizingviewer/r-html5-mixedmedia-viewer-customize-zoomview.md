---
title: Exibição de zoom
description: No modo de zoom contínuo, a exibição principal consiste na imagem com zoom quando o ativo atual é uma única imagem.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
TQID: 'https://experienceleague.adobe.com/xfQKn46HParEFKYh1jrrVxbmkUKQHJbcWlJ7LWHIsc0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# Exibição de zoom{#zoom-view}

No modo de zoom contínuo, a exibição principal consiste na imagem com zoom quando o ativo atual é uma única imagem.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo no formato hexadecimal da janela principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>O cursor exibido sobre a visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição de zoom transparente.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Em sistemas desktop, o componente oferece suporte ao seletor de atributos `cursortype` que pode ser aplicado à classe `.s7zoomview`. Ele controla o tipo de cursor com base no estado do componente e na ação do usuário. Os seguintes valores `cursortype` têm suporte:

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
