---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic Media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 1%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Atributo de configuração para o Visualizador de vídeo interativo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|esquerda|direita  </span> </p> </td> 
   <td colname="col2"> <p> Especifica a forma como as amostras são preenchidas na visualização. </p> <p>Defina para <span class="codeph"> esquerda </span> para definir a ordem de preenchimento da esquerda para a direita. </p> <p>Definir para <span class="codeph"> direita </span> inverte a ordem para que a visualização seja preenchida na direção direita para esquerda, de cima para baixo. </p> <p>Quando <span class="codeph"> auto </span> está definido, o componente aplica o modo direito quando locale está definido como " <span class="codeph"> ja </span>"; caso contrário, <span class="codeph"> left </span> será usado. </p> </td> 
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

