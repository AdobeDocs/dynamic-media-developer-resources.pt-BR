---
description: Imagem do mapa de brilho. Fornece controle pixel-por-pixel do brilho de uma textura repetível, papel de parede/borda ou decalque.
seo-description: Imagem do mapa de brilho. Fornece controle pixel-por-pixel do brilho de uma textura repetível, papel de parede/borda ou decalque.
seo-title: glossário
solution: Experience Manager
title: glossário
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# glossmap{#glossmap}

Imagem do mapa de brilho. Fornece controle pixel-por-pixel do brilho de uma textura repetível, papel de parede/borda ou decalque.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;trace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossárioMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Arquivo de imagem do mapa de brilho (escala de cinza). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Solicitação para o servidor de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Solicitação para um servidor externo. </p></td> 
 </tr> 
</table>

Aplicável a materiais como efeitos de tintas metálicas, papel de parede de folha cortada em série e bordas, tecidos de fios metálicos e assim por diante.

A imagem do mapa de brilho deve ser em tons de cinza de 8 bits e ter exatamente o mesmo tamanho da imagem primária especificada com `src=`. Consulte a descrição de [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter mais informações.

## Propriedades {#section-26375672d69849be9b026cc93c3bc558}

Atributo de material. Suportado por texturas, papéis de parede e bordas repetíveis e decalques. Ignorado por materiais de revestimento de cor sólida, armário e janela. Consulte [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter mais informações.

## Padrão {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nenhum.

## Consulte também {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
