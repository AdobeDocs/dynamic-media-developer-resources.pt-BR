---
description: Imagem do mapa de brilho. Fornece controle pixel por pixel da luminosidade de uma textura repetível, papel de parede/borda ou decal.
seo-description: Imagem do mapa de brilho. Fornece controle pixel por pixel da luminosidade de uma textura repetível, papel de parede/borda ou decal.
seo-title: glossário
solution: Experience Manager
title: glossário
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# glossmap{#glossmap}

Imagem do mapa de brilho. Fornece controle pixel por pixel da luminosidade de uma textura repetível, papel de parede/borda ou decal.

`glossmap={ *``*| *`glossMapFilebeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;laço;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Arquivo de imagem do mapa de brilho (escala de cinza). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Solicitar ao servidor de imagens. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Solicitar a um servidor externo. </p></td> 
 </tr> 
</table>

Aplicável a materiais como efeitos de tinta metálica, papéis de parede de folha cortada sob tinta e bordas, tecidos metálicos de fio, e assim por diante.

A imagem do mapa de brilho deve ter uma escala de cinza de 8 bits e ter exatamente o mesmo tamanho que a imagem principal especificada com `src=`. Consulte a descrição de [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter mais informações.

## Propriedades {#section-26375672d69849be9b026cc93c3bc558}

Atributo material. Suportado por texturas repetíveis, papéis de parede e bordas e decalques. Ignorados por materiais de revestimento de cor sólida, armário e janela. Consulte [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter mais informações.

## Padrão {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nenhum.

## Consulte também {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
