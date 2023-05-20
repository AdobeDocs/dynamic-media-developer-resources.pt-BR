---
title: glossmap
description: Imagem do mapa de brilho. Fornece controle pixel por pixel da textura brilhante, papel de parede/borda ou decalque repetíveis.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# glossmap {#glossmap}

Imagem do mapa de brilho. Fornece controle pixel por pixel da textura brilhante, papel de parede/borda ou decalque repetíveis.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Arquivo de imagem do mapa de brilho (escala de cinza). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Solicitação para o servidor de imagens. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ForeignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Solicitação para um servidor externo. </p></td> 
 </tr> 
</table>

Aplicável para materiais como efeitos de tinta metálica, papel de parede e bordas de folha de corte e tecidos de fio metálicos.

A imagem do mapa de brilho deve ser em tons de cinza de 8 bits e ter o mesmo tamanho que a imagem principal especificada com `src=`. Consulte a descrição de [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter informações adicionais.

## Propriedades {#section-26375672d69849be9b026cc93c3bc558}

Atributo de material. Suportado por texturas repetíveis, papéis de parede e bordas, e decalques. Ignorado por materiais sólidos de cor, gabinete e revestimento de janela. Consulte [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) para obter informações adicionais.

## Padrão {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nenhum.

## Consulte também {#section-33953fc1be82452da37141f2e541e00c}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
