---
description: Cor da camada. Especifica a cor de primeiro plano e a opacidade das camadas de cor sólida e efeito, e a cor de preenchimento da caixa de texto para as camadas de texto.
seo-description: Cor da camada. Especifica a cor de primeiro plano e a opacidade das camadas de cor sólida e efeito, e a cor de preenchimento da caixa de texto para as camadas de texto.
seo-title: color
solution: Experience Manager
title: color
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# color{#color}

Cor da camada. Especifica a cor de primeiro plano e a opacidade das camadas de cor sólida e efeito, e a cor de preenchimento da caixa de texto para as camadas de texto.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de cor cinza, RGB ou CMYK, com ou sem alfa. </p> </td> 
 </tr> 
</table>

No caso de camadas de imagem e texto, `color=` preenche as áreas transparentes e semiopacas dentro do retângulo delimitador da camada com a cor especificada* antes de* `rotate=` e `extend=` serem aplicadas.

## Propriedades {#section-d6e74c36a49547849212e4db8927e678}

Atributo de camada. Aplica-se à camada atual ou à camada 0 se `layer=comp`.

*`color`* presume-se que existe no espaço de cores de trabalho correspondente ao tipo de pixel de  *`color`*. *`color`* é convertida com precisão se a imagem da camada tiver um tipo de pixel diferente no momento da mesclagem.

## Padrão {#section-60611c72876b4c45b5c85ce35608e5ec}

Sem predefinição para camadas sólidas de cor e efeito; uma cor deve ser especificada. O padrão é 0,0,0,0 (totalmente transparente) para camadas de imagem e texto.

## Exemplo {#section-2d090493f4ec4e188bbc5565aa151a05}

No fragmento de modelo a seguir, definimos o plano de fundo do texto para uma cor 50% opaca e usamos a mesma cor para adicionar uma borda de 10 pixels semitransparente ao redor da imagem da camada 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Consulte também {#section-f0e059f857b64b61ab4f23312b8dc619}

[cor](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Gerenciamento de  [cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
