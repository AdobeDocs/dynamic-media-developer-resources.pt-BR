---
description: Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# textAttr{#textattr}

Atributos da camada de texto. Especifica atributos adicionais para camadas de texto que não estão disponíveis como comandos rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Fornece um meio de dimensionar a camada de texto sem alterar tamanhos de fonte. Valores de resolução mais alta aumentam o tamanho do texto renderizado em relação ao tamanho da tela; valores menores reduzem o tamanho do texto. Resolução do texto em pontos por polegada (int maior que 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla o modo anti-aliasing usado pelo mecanismo de renderização de texto. </p> <p> <span class="codeph"> off | norma | estaladiça | afiada | forte | liso  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off  </span> </p> </td> 
      <td class="stentry"> <p>Desative a suavização de texto. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma  </span> </p> </td> 
      <td class="stentry"> <p>Ativar o modo de suavização de texto padrão (padrão). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> estalo  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo anti-aliasing Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> apenas). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nítido  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo anti-aliasing Photoshop <span class="codeph"> nítido </span> ( <span class="codeph"> textPs= </span> apenas). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> forte  </span> </p> </td> 
      <td class="stentry"> <p>Selecione o modo anti-aliasing Photoshop <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> somente). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controla como a res é usada ao renderizar o texto </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Use a resolução especificada. </p> <p>Use se o texto for renderizado em um tamanho exato em relação à tela de composição. O texto pode ser recortado para o tamanho da camada (se especificado) se a caixa de texto for muito pequena. Esta é a única opção <span class="varname"> resMode </span> suportada por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Ajuste a resolução automaticamente para melhor preencher o reto da camada com o texto. </p> <p>Use para ajustar automaticamente o tamanho do texto de forma que a caixa de texto seja preenchida o máximo possível, sem risco de truncamento. Se a quebra automática de texto estiver ativada, o texto poderá ser reenvolvido na resolução final. <span class="varname"> res  </span> é ignorado se  <span class="codeph"> autoRes  </span> estiver selecionado. Não suportado por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilizar a resolução especificada; diminua-o se necessário para impedir que o texto seja truncado no retângulo da camada. </p> <p>Use para renderizar o texto na resolução especificada exata, desde que não haja recorte. No caso de recorte, a resolução é automaticamente reduzida para garantir que todo o texto esteja contido totalmente dentro da caixa de texto. Se a quebra automática de texto estiver ativada, o texto poderá ser reenvolvido na resolução final. Não suportado por <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se o tamanho da camada de texto não for especificado com size= ou se somente a largura for especificada, as configurações de 'autoRes' e 'maxRes' serão ignoradas e a resolução especificada será usada para renderizar o texto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica o modo de encapsulamento. </p> <p> <span class="codeph"> quebra | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Desativar quebra automática de linha. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> quebra  </span> </p> </td> 
      <td class="stentry"> <p>Habilitar quebra automática de texto padrão. </p> <p>Quebra palavras longas, se necessário. <span class="codeph"> textPs= suporta  </span> apenas  <span class="codeph"> quebra automática  </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Habilitar quebra de linha. </p> <p>Nunca quebra uma palavra, mesmo que ela fique truncada no final. Normalmente usado em conjunto com <span class="codeph"> autoRes </span> ou <span class="codeph"> maxRes </span> para garantir que palavras longas nunca sejam quebradas. </p> </td> 
     </tr> 
    </table> </p> <p>Ambos <span class="codeph"> envolvem </span> e <span class="codeph"> embrulham </span> automaticamente nos limites de palavras e hífens. </p> </td> 
 </tr> 
</table>

## Propriedades {#section-114ca0b8585b403c873e2251478ad1d5}

Atributo de camada de texto. Ignorado por imagem, cor sólida e camadas de efeito. Aplica-se a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consulte também {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
