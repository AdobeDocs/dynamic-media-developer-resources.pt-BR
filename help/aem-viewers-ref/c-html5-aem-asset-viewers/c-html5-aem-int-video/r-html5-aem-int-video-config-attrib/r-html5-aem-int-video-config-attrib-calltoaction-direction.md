---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---

# CallToAction.direction{#calltoaction-direction}

Atributo de configuração para o Visualizador de vídeo interativo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|esquerda|direita  </span> </p> </td> 
   <td colname="col2"> <p> Especifica a forma como as miniaturas são preenchidas na exibição. </p> <p>Defina como <span class="codeph"> à esquerda </span> para definir a ordem de preenchimento da esquerda para a direita. </p> <p>Definir para <span class="codeph"> direita </span> inverte a ordem para que a exibição seja preenchida na direção direita para a esquerda, de cima para baixo. </p> <p>Defina como <span class="codeph"> auto </span> para que o componente aplique o modo direito quando a localidade estiver definida como <span class="codeph"> "ja" </span>; caso contrário, <span class="codeph"> à esquerda </span> será usado. </p> </td> 
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
