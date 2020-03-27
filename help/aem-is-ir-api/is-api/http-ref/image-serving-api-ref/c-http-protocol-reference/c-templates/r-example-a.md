---
description: Crie um modelo de tamanho fixo com uma imagem de plano de fundo estática, uma imagem variável alinhada ao plano de fundo no centro esquerdo e dimensionada para não exceder 80% da largura e altura do plano de fundo, e uma camada de texto com texto vertical centralizado na borda direita da tela.
seo-description: Crie um modelo de tamanho fixo com uma imagem de plano de fundo estática, uma imagem variável alinhada ao plano de fundo no centro esquerdo e dimensionada para não exceder 80% da largura e altura do plano de fundo, e uma camada de texto com texto vertical centralizado na borda direita da tela.
seo-title: Exemplo A
solution: Experience Manager
title: Exemplo A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Exemplo A{#example-a}

Crie um modelo de tamanho fixo com uma imagem de plano de fundo estática, uma imagem variável alinhada ao plano de fundo no centro esquerdo e dimensionada para não exceder 80% da largura e altura do plano de fundo, e uma camada de texto com texto vertical centralizado na borda direita da tela.

![](assets/examplea.png)

## O registro do modelo {#section-32f54710593e438fa0622224c89380af}

Inserir objeto

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo:Modificador </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0,5,0&amp;posN=-0,5,0&amp; layer=2&amp;$text=layer+2+text+go+here&amp;text=rtext tf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

Os `origin=` valores de todas as camadas são especificados explicitamente no modelo para controlar rigorosamente o posicionamento e o alinhamento das camadas. Cada origem de camada é definida para corresponder ao alinhamento desejado para essa camada. O plano `origin=` de fundo (camada 0) está definido para o centro; isso é arbitrário, pois a imagem de fundo não será alterada em tempo de execução; qualquer valor para a origem da camada 0 pode ser usado.

Os `pos=` valores fornecem os deslocamentos necessários entre os pontos de origem da camada, para alcançar o posicionamento desejado da camada.

A âncora da imagem da camada 1 é colocada no centro esquerdo; juntamente com o `pos=` valor, isso atinge o alinhamento no centro esquerdo entre o plano de fundo e a imagem da camada 1, independentemente da proporção da imagem da camada 1.

Da mesma forma, a âncora da camada de texto é posicionada no centro direito da caixa de texto de tamanho automático. Em conjunto com pos= isso atinge o alinhamento desejado do centro direito para o texto girado, independentemente do tamanho da fonte e do comprimento da string.

O texto de exibição real será fornecido em tempo de execução, de modo que uma variável é usada para separar o texto do envelope de formatação rtf. Usamos a variável padrão `$object` para a imagem da camada 1. Isso permite especificar essa imagem no caminho da solicitação.

Qualquer imagem pode ser usada para a imagem de plano de fundo e para a imagem da camada 1. Se a imagem de plano de fundo tiver uma máscara, as áreas não mascaradas serão preenchidas com a cor de plano de fundo padrão ( `attribute::BkgColor`) ou deixadas transparentes quando `fmt=png-alpha` ou `fmt=tif-alpha`. Se a imagem de plano de fundo tiver uma proporção não quadrada, ela será centralizada na imagem de resposta e o espaço extra será preenchido `attribute::BkgColor`. Se a imagem da camada 1 tiver dados alfa ou uma máscara, a imagem de plano de fundo (ou cor de plano de fundo) permanecerá visível nas áreas transparentes. Se a imagem não tiver máscara, ela preencherá todo o retângulo alocado.

## Uso do modelo {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

A ilustração a seguir mostra o resultado composto para diferentes proporções da imagem da camada 1 e diferentes sequências de texto.

![](assets/exampleausing.png)

