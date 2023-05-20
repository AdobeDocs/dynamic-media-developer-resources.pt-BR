---
title: CallToAction.direction
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# CallToAction.direction{#calltoaction-direction}

Atributo de configuração para o Visualizador de vídeo interativo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Especifica como as miniaturas são preenchidas na exibição. </p> <p>Defina como <span class="codeph"> left </span> para definir a ordem de preenchimento da esquerda para a direita. </p> <p>Defina como <span class="codeph"> direita </span> inverte a ordem para que a vista seja preenchida da direita para a esquerda, de cima para baixo. </p> <p>Defina como <span class="codeph"> automático </span> para que o componente aplique o modo correto quando a localidade estiver definida como <span class="codeph"> "ja" </span>; caso contrário, <span class="codeph"> left </span> é usada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
