---
description: O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.
seo-description: O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.
seo-title: Player Video360
solution: Experience Manager
title: Player Video360
topic: Dynamic Media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Player Video360{#video-player}

O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões do vídeo que está sendo reproduzido não corresponderem às dimensões do player de vídeo, o conteúdo do vídeo será centralizado na área de exibição do retângulo do player de vídeo.

O seletor de classe CSS a seguir controla a aparência do player de vídeo:

```
.s7video360viewer .s7video360player
```

**Propriedades de CSS do player de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode localizar a mensagem de erro exibida nos casos em que o sistema não consegue reproduzir o vídeo.

Consulte [Localização de elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exemplo - Para configurar um visualizador de vídeo com o tamanho do player de vídeo definido como 512 x 288 pixels.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

A aparência da animação de buffering é controlada com o seguinte seletor de classe CSS:

```
.s7video360viewer .s7video360player .s7waiticon
```

**Propriedades CSS do ícone de espera**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> Altura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p> Margem esquerda do ícone Animação, normalmente menos metade da largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p> Margem superior do ícone de animação, normalmente menos metade da altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Nódulo de arte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma animação de buffering para ter 101 pixels de largura, 29 pixels de altura:

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

