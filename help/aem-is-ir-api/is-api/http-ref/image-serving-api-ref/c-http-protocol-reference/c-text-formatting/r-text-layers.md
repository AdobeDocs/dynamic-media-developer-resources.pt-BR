---
description: textPs= suporta vários modelos de uso diferentes descritos nesta seção.
seo-description: textPs= suporta vários modelos de uso diferentes descritos nesta seção.
seo-title: Camadas de texto
solution: Experience Manager
title: Camadas de texto
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Camadas de texto{#text-layers}

textPs= suporta vários modelos de uso diferentes descritos nesta seção.

>[!NOTE]
>
>Esta seção não se aplica a `text=`.

As regras e definições comuns são as seguintes:

* Camadas de texto de autodimensionamento são camadas que não incluem um comando `size=` ou para as quais `size=0,0` é especificado.

* O tamanho da camada das camadas de texto de autodimensionamento é determinado pelo texto real renderizado.
* A âncora de camada padrão das camadas de texto de autodimensionamento geralmente está *e não* no centro da camada (veja abaixo).
* Se `anchor=` ou `origin=` for especificado para camadas de texto de autodimensionamento, a posição da camada de texto será influenciada pelo conteúdo do texto.

* Quando `size=` for especificado, partes de glifos de caracteres poderão ser renderizadas fora do retângulo de camada.
* `pos=` pode ser usado em todos os casos para reposicionar uma camada de texto.

## Texto pontual (autodimensionamento) {#section-db99ec98eb114458b2dbc9911a58f74a}

O texto do ponto estilo Photoshop é simulado quando `textPs=` é especificado sem `size=`, `textPath=` ou `textFlowPath=`. O tamanho da camada é determinado horizontalmente pela largura do texto renderizado e verticalmente pelo espaçamento entre linhas. O texto nunca será quebrado automaticamente.

Se `anchor=` ou `origin=` não forem especificados, a primeira linha do texto será posicionada imediatamente acima da origem da camada; os parágrafos marcados com `\ql` são posicionados à direita da origem da camada, os parágrafos que incluem `\qr` são renderizados à esquerda da origem e os parágrafos com `\qc` são centralizados horizontalmente em torno da origem. As regras de posicionamento de camada padrão se `anchor=` ou `origin=` forem especificadas.

Se `color=` for especificado, preencherá a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Caixa de texto retangular {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` for especificado além de `textPs=` (sem `textPath=` e `textFlowPath=`), o texto será restrito ao retângulo especificado. A camada é posicionada como de costume. Os glifos de caractere próximos às bordas da caixa de texto podem ser renderizados parcialmente fora da caixa de texto.

`color=` preenche a região definida por  `size=`.

Todos os comandos RTF são aplicados como esperado.

## Caixa de texto de altura variável {#section-e1233d1c9f8e43218667361dc0c4fd06}

A especificação de `size=` com altura 0 permite que a caixa de texto seja dimensionada verticalmente para acomodar todo o conteúdo. A largura da camada é definida pela largura de `size=` e a altura da camada pela altura do texto renderizado real. A camada é posicionada como de costume. Os glifos de caracteres próximos às bordas esquerda e direita da caixa de texto podem ser renderizados parcialmente fora da caixa de texto.

`color=` preenche o retângulo definido pela largura especificada com  `size=` e a altura do texto real renderizado.

Os seguintes comandos RTF são ignorados:

`\vertal*`

## Texto de autodimensionamento no caminho {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` juntamente com  `textPs=` podem ser usadas para definir uma ou mais regiões nas quais o texto deve ser continuado. `textFlowXPath=` pode ser especificado opcionalmente para excluir o texto do fluxo para uma ou mais áreas. Se `size=` não for especificado, a camada de texto resultante será autodimensionada e o tamanho da camada será determinado pela caixa delimitadora do texto realmente renderizado.

Se `origin=` nem `anchor=` não forem especificados, a âncora de camada assumirá (0,0) o espaço de coordenadas de pixel usado para definir os caminhos, garantindo o posicionamento absoluto independentemente do texto renderizado. Se `anchor=` ou `origin=` forem especificados, a camada será posicionada em relação à caixa delimitadora do conteúdo real renderizado (e se adaptará a ela).

`color=` preenche a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados:

`\marg*`

## Texto pré-dimensionado no caminho {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` for especificado junto com `textFlowPath=`, o tamanho da camada será pré-determinado. (0,0) do espaço de coordenadas de pixels usado para definir os caminhos está localizado no canto superior esquerdo do retângulo de camada.

As regiões `textFlowPath=` podem estar localizadas fora do retângulo da camada. O texto sempre será continuado e renderizado em todas as regiões de caminho, mesmo se isso resultar na renderização do texto fora do retângulo da camada. `extend=0,0,0,0`pode ser usado para recortar o texto renderizado no retângulo da camada.

Para fins de posicionamento de camada, o retângulo de camada é baseado no `size=` especificado, independentemente de quanto texto é realmente renderizado, mesmo se algum estiver localizado fora do retângulo de camada. O posicionamento padrão da camada se aplica.

`color=` preenche a área retangular definida por  `size=`.

Os seguintes comandos RTF são ignorados para `textFlowPath=`:

`\marg*`

## Texto de autodimensionamento no caminho {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define um ou mais caminhos nos quais o texto especificado com  `textPs=` deve ser renderizado. Quando `size=` não for especificado, a camada de texto resultante será de autodimensionamento. O tamanho da camada é determinado pela caixa delimitadora do texto real renderizado.

Se `origin=` nem `anchor=` não forem especificados, a âncora de camada assumirá (0,0) o espaço de coordenadas de pixel usado para definir o caminho; a posição do texto renderizado é fixa independentemente de quanto texto é renderizado. Se `anchor=` ou `origin=` forem especificados, a camada será posicionada em relação à caixa delimitadora do conteúdo real renderizado (e se adaptará a ela).

`color=` preenche a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualquer texto após o primeiro `\par` ou `\line` é ignorado.

## Texto pré-dimensionado no caminho {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` for especificado junto com `textPath=`, o tamanho da camada será pré-determinado. (0,0) do espaço de coordenadas de pixels usado para definir os caminhos está localizado no canto superior esquerdo do retângulo de camada.

Os caminhos podem estar localizados parcial ou totalmente fora do retângulo da camada. O texto sempre será aplicado e renderizado ao longo de todo o caminho, mesmo se estiver fora do retângulo da camada. `extend=0,0,0,0` pode ser usado para recortar o texto renderizado no retângulo da camada.

Para fins de posicionamento de camada, o retângulo de camada é baseado no `size=` especificado, mesmo se algum texto for renderizado fora do retângulo de camada. O posicionamento padrão da camada se aplica.

`color=` preenche a área definida por  `size=`.

Os seguintes comandos RTF são ignorados:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualquer texto após o primeiro `\par` ou `\line` é ignorado.
