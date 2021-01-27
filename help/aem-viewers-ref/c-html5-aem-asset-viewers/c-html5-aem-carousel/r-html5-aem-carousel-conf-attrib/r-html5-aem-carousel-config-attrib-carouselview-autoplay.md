---
description: Atributo de configuração para o Visualizador do carrossel.
seo-description: Atributo de configuração para o Visualizador do carrossel.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic Media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---


# CarouselView.autoplay{#carouselview-autoplay}

Atributo de configuração para o Visualizador do carrossel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duração][,direção]</span> </p> </td> 
   <td colname="col2"> <p> Especifica liga/desliga, duração para exibir cada banner no carrossel e direção do loop automático. </p> <p>Defina como <span class="codeph"> 0</span> para desligar o loop automático. </p> <p>Defina <span class="codeph"> 1</span> para efetuar o loop automático com a duração da transição em segundos controlados por <span class="codeph"> duração</span>. </p> <p>A direção do loop automático é controlada com <span class="codeph"> direção</span>. A direção <span class="codeph"></span> tem o intervalo entre <span class="codeph"> 1</span> da direita para a esquerda e <span class="codeph"> 0</span> da esquerda para a direita. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```

