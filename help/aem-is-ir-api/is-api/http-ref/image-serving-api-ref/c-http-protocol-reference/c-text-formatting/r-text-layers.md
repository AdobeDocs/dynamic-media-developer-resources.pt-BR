---
description: textPs= suporta vários modelos de uso diferentes descritos nesta seção.
solution: Experience Manager
title: Camadas de texto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Camadas de texto{#text-layers}

textPs= suporta vários modelos de uso diferentes descritos nesta seção.

>[!NOTE]
>
>Esta seção não se aplica a `text=`.

As regras comuns e as definições são as seguintes:

* Camadas de texto de autodimensionamento são camadas que não incluem um comando `size=` ou para as quais `size=0,0` é especificado.

* O tamanho da camada de camadas de texto de autodimensionamento é determinado pelo texto real renderizado.
* A âncora de camada padrão de camadas de texto de autodimensionamento geralmente é *não* no centro da camada (veja abaixo).
* Se `anchor=` ou `origin=` for especificado para camadas de texto de autodimensionamento, a posição da camada de texto será influenciada pelo conteúdo do texto.

* Quando `size=` é especificado, partes de glifos de caracteres podem ser renderizadas fora do retângulo da camada.
* `pos=` pode ser usado em todos os casos para reposicionar uma camada de texto.

## Texto pontual (autodimensionamento) {#section-db99ec98eb114458b2dbc9911a58f74a}

O texto de ponto de estilo Photoshop é simulado quando `textPs=` é especificado sem `size=`, `textPath=` ou `textFlowPath=`. O tamanho da camada é determinado horizontalmente pela largura do texto renderizado e verticalmente pelo espaçamento entre linhas. O texto nunca é quebrado automaticamente.

Se nem `anchor=` nem `origin=` forem especificados, a primeira linha do texto será posicionada imediatamente acima da origem da camada; parágrafos marcados com `\ql` serão posicionados à direita da origem da camada, parágrafos que incluem `\qr` serão renderizados à esquerda da origem e parágrafos com `\qc` serão centralizados horizontalmente em torno da origem. As regras de posicionamento de camada padrão se aplicam se `anchor=` ou `origin=` forem especificados.

Se `color=` for especificado, ele preencherá a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Caixa de texto retangular {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` for especificado além de `textPs=` (sem `textPath=` e `textFlowPath=`), o texto será restrito ao retângulo especificado. A camada é posicionada como de costume. Os glifos de caracteres próximos às bordas da caixa de texto podem ser renderizados parcialmente fora dela.

`color=` preenche a região definida por `size=`.

Todos os comandos RTF são aplicados conforme esperado.

## Caixa de texto Altura variável {#section-e1233d1c9f8e43218667361dc0c4fd06}

Especificar `size=` com altura 0 permite que a caixa de texto seja dimensionada verticalmente para acomodar todo o conteúdo. A largura da camada é definida pela largura de `size=`, e a altura da camada pela altura do texto renderizado real. A camada é posicionada como de costume. Os glifos de caracteres próximos às bordas esquerda e direita da caixa de texto podem ser renderizados parcialmente fora dela.

`color=` preenche o retângulo definido pela largura especificada com `size=` e a altura do texto real renderizado.

Os seguintes comandos RTF são ignorados:

`\vertal*`

## Texto de autodimensionamento no caminho {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` em conjunto com `textPs=` pode ser usado para definir uma ou mais regiões nas quais o texto deve fluir. `textFlowXPath=` pode ser especificado opcionalmente para excluir o fluxo de texto para uma ou mais áreas. Se `size=` não for especificado, a camada de texto resultante terá autodimensionamento e o tamanho da camada será determinado pela caixa delimitadora do texto realmente renderizado.

Se `origin=` e `anchor=` não forem especificados, a âncora de camada assumirá como padrão (0,0) do espaço de coordenadas em pixels usado para definir o(s) caminho(s), garantindo o posicionamento absoluto independentemente do texto renderizado. Se `anchor=` ou `origin=` forem especificados, a camada será posicionada em relação à (e adaptando-se à) caixa delimitadora do conteúdo real renderizado.

`color=` preenche a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados:

`\marg*`

## Texto pré-dimensionado no caminho {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` for especificado junto com `textFlowPath=`, o tamanho da camada será predeterminado. (0,0) do espaço de coordenadas em pixels usado para definir o(s) caminho(s) está localizado no canto superior esquerdo do retângulo da camada.

As regiões `textFlowPath=` podem estar localizadas fora do retângulo da camada. O texto sempre flui e é renderizado em todas as regiões do caminho, mesmo que isso resulte na renderização do texto fora do retângulo da camada. `extend=0,0,0,0`pode ser usado para cortar o texto renderizado no retângulo da camada.

Para fins de posicionamento de camadas, o retângulo da camada é baseado no `size=` especificado, independentemente da quantidade de texto que é realmente renderizado, mesmo que parte dele esteja localizada fora do retângulo da camada. O posicionamento de camada padrão é aplicável.

`color=` preenche a área retangular definida por `size=`.

Os seguintes comandos RTF são ignorados para `textFlowPath=`:

`\marg*`

## Dimensionamento automático de texto no caminho {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` define um ou mais caminhos nos quais o texto especificado com `textPs=` deve ser renderizado. Quando `size=` não é especificado, a camada de texto resultante é de autodimensionamento. O tamanho da camada é determinado pela caixa delimitadora do texto real renderizado.

Se nem `origin=` nem `anchor=` forem especificados, a âncora de camada assumirá como padrão (0,0) o espaço de coordenadas em pixels usado para definir o caminho; a posição do texto renderizado é fixa independentemente de quanto texto é renderizado. Se `anchor=` ou `origin=` forem especificados, a camada será posicionada em relação à (e adaptando-se à) caixa delimitadora do conteúdo real renderizado.

`color=` preenche a caixa delimitadora do texto real renderizado.

Os seguintes comandos RTF são ignorados:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualquer texto após o primeiro `\par` ou `\line` é ignorado.

## Texto pré-dimensionado no caminho {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` for especificado junto com `textPath=`, o tamanho da camada será predeterminado. (0,0) do espaço de coordenadas em pixels usado para definir o(s) caminho(s) está localizado no canto superior esquerdo do retângulo da camada.

Os caminhos podem estar localizados parcial ou totalmente fora do retângulo da camada. O texto é sempre aplicado e renderizado ao longo de todo o caminho, mesmo se estiver fora do retângulo da camada. `extend=0,0,0,0` pode ser usado para cortar o texto renderizado no retângulo da camada.

Para fins de posicionamento de camada, o retângulo de camada é baseado no `size=` especificado, mesmo que parte do texto seja renderizado fora do retângulo de camada. O posicionamento de camada padrão é aplicável.

`color=` preenche a área definida por `size=`.

Os seguintes comandos RTF são ignorados:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualquer texto após o primeiro `\par` ou `\line` é ignorado.
