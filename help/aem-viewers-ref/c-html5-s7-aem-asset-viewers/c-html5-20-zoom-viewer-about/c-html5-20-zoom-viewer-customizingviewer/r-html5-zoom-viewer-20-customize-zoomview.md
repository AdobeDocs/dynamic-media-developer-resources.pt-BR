---
title: Exibição de zoom
description: A visualização principal consiste na imagem com zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
TQID: 'https://experienceleague.adobe.com/i1B2r5g74xmk6H3DLD12gyRI9uJo32p3SmgS-OFnLf8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 171
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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
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

