---
description: Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.
seo-description: Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---


# textAttr{#textattr}

Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Fornece um meio de dimensionar a camada de texto sem alterar tamanhos de fonte. Valores de resolução mais alta aumentam o tamanho do texto renderizado em relação ao tamanho da tela de desenho; valores menores reduzem o tamanho do texto. Resolução de texto em pontos por polegada (int maior que 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> suavização de serrilhado  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla o modo de suavização de borda usado pelo mecanismo de renderização de texto. </p> <p> <span class="codeph"> off | norma | nítida | afiada | forte | liso  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off  </span> </p> </td> 
      <td class="stentry"> <p>Desative a suavização de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma  </span> </p> </td> 
      <td class="stentry"> <p>Ative o modo de suavização de texto padrão (padrão). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> estalo  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo de suavização de borda Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> apenas). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> agudo  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo de suavização de borda Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> apenas). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> forte  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo de suavização de borda Photoshop <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> apenas). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla como a res é usada ao renderizar o texto </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Use a resolução especificada. </p> <p>Use se o texto for renderizado em um tamanho exato em relação à tela de composição. O texto pode ser cortado para o tamanho da camada (se especificado) se a caixa de texto for muito pequena. Esta é a única opção <span class="varname"> resMode </span> suportada por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Ajuste a resolução automaticamente para melhor preencher o retângulo de camada com o texto. </p> <p>Use para ajustar automaticamente o tamanho do texto de forma que a caixa de texto seja preenchida o máximo possível, sem risco de truncamento. Se a quebra automática de texto estiver ativada, o texto poderá ser reencapsulado na resolução final. <span class="varname"> res  </span> é ignorado se  <span class="codeph"> autoRes  </span> estiver selecionado. Não suportado por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilizar a resolução especificada; diminua-o se necessário para impedir que o texto seja truncado no retângulo da camada. </p> <p>Use para renderizar o texto na resolução especificada exata, contanto que nenhum recorte ocorra. No caso de recorte, a resolução é automaticamente diminuída para garantir que todo o texto esteja contido totalmente dentro da caixa de texto. Se a quebra automática de texto estiver ativada, o texto poderá ser reencapsulado na resolução final. Não suportado por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se o tamanho da camada de texto não for especificado com size= ou se apenas a largura for especificada, as configurações 'autoRes' e 'maxRes' serão ignoradas e a resolução especificada será usada para renderizar o texto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica o modo de quebra automática. </p> <p> <span class="codeph"> moldura | noWrap | nbQuebra automática  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Desabilitar quebra automática de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> moldura  </span> </p> </td> 
      <td class="stentry"> <p>Habilitar quebra automática padrão. </p> <p>Quebra longas palavras, se necessário. <span class="codeph"> textPs=  </span> só suporta  <span class="codeph"> quebra automática  </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Habilitar quebra automática de texto. </p> <p>Nunca quebra uma palavra, mesmo que ela fique truncada no final. Normalmente usado em conjunto com <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> para garantir que palavras longas nunca sejam quebradas. </p> </td> 
     </tr> 
    </table> </p> <p>Ambas as <span class="codeph"> vinculam </span> e <span class="codeph"> embrulham </span> automaticamente nos limites de palavras e hífens. </p> </td> 
 </tr> 
</table>

## Propriedades {#section-114ca0b8585b403c873e2251478ad1d5}

Atributo de camada de texto. Ignorado por imagem, cor sólida e camadas de efeito. Aplica-se a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consulte também {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
