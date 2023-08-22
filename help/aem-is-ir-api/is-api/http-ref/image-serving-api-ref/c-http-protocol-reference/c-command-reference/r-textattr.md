---
title: textAttr
description: Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# textAttr{#textattr}

Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>Fornece um meio de dimensionar a camada de texto sem alterar os tamanhos de fonte. Valores de resolução mais altos aumentam o tamanho do texto renderizado em relação ao tamanho da tela de desenho; valores menores reduzem o tamanho do texto. Resolução do texto em pontos por polegada (int maior que 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla o modo de suavização de serrilhado empregado pelo mecanismo de renderização de texto. </p> <p> <span class="codeph"> desligado | norma | estaladiço | sustenido | forte | suave </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> desligado </span> </p> </td> 
      <td class="stentry"> <p>Desativar a suavização de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
      <td class="stentry"> <p>Ativar o modo de suavização de texto padrão (padrão). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nítido </span> </p> </td> 
      <td class="stentry"> <p>Selecionar modo de suavização de borda do Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> somente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sharp </span> </p> </td> 
      <td class="stentry"> <p>Selecionar modo de suavização de borda do Photoshop <span class="codeph"> sharp </span> ( <span class="codeph"> textPs= </span> somente). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> forte </span> </p> </td> 
      <td class="stentry"> <p>Selecionar modo de suavização de borda do Photoshop <span class="codeph"> forte </span> ( <span class="codeph"> textPs= </span> somente). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla como res é usado ao renderizar o texto </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Use a resolução especificada. </p> <p>Use se o texto deve ser renderizado em um tamanho exato em relação à tela de composição. O texto pode ser recortado para o tamanho da camada (se especificado) se a caixa de texto for muito pequena. Este é o único <span class="varname"> resMode </span> opção compatível com o <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Ajuste a resolução automaticamente para preencher melhor a camada com o texto. </p> <p>Use para ajustar automaticamente o tamanho do texto para que a caixa de texto seja preenchida o máximo possível, sem risco de truncamento. Se a quebra de linha estiver ativa, o texto poderá ser requebrado na resolução final. <span class="varname"> res </span> é ignorado se <span class="codeph"> autoRes </span> está selecionada. Não compatível com o <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Use a resolução especificada; diminua-a, se necessário, para impedir que o texto seja truncado na camada de retângulo. </p> <p>Use para renderizar o texto na resolução especificada exata, desde que não ocorra recorte. No caso de recorte, a resolução é automaticamente diminuída para garantir que todo o texto esteja totalmente contido dentro da caixa de texto. Se a quebra de linha estiver ativa, o texto poderá ser requebrado na resolução final. Não compatível com o <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se o tamanho da camada de texto não for especificado com size= ou se apenas a largura for especificada, as configurações "autoRes" e "maxRes" serão ignoradas e a resolução especificada será usada para renderizar o texto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica o modo de encapsulamento. </p> <p> <span class="codeph"> quebra automática | semQuebra | nbQuebra </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Desative a quebra automática de linha. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> quebra automática </span> </p> </td> 
      <td class="stentry"> <p>Ativar quebra automática de linha padrão. </p> <p>Quebra palavras longas se necessário. <span class="codeph"> textPs= </span> apenas suporta <span class="codeph"> quebra automática </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Ativar quebra automática de linha. </p> <p>Nunca quebra uma palavra, mesmo que ela fique truncada no final. Normalmente usada em conjunto com <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> para garantir que palavras longas nunca sejam quebradas. </p> </td> 
     </tr> 
    </table> </p> <p>Ambos <span class="codeph"> quebra automática </span> e <span class="codeph"> nbwrap </span> quebra automática de linha em limites de palavras e hifens. </p> </td> 
 </tr> 
</table>

## Propriedades {#section-114ca0b8585b403c873e2251478ad1d5}

Atributo de camada de texto. Ignorado por camadas de imagem, cor sólida e efeito. Aplicável a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consulte também {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
