---
description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.
seo-description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.
seo-title: Restrições e problemas conhecidos
solution: Experience Manager
title: Restrições e problemas conhecidos
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 0%

---


# Restrições e problemas conhecidos{#restrictions-and-known-issues}

Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.

## Erro de documentação {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* O número de linhas não excederá o máximo da configuração `\copyfitmaxlines` e o número de linhas explícitas na entrada de texto.
* São necessários parênteses e colchetes correspondentes em conjuntos de imagens. Se as chaves e os parênteses não corresponderem, eles precisarão ser codificados no URL.
* O alerta de tempo de resposta global do lado do servidor inclui respostas de erro.
* O comando `id=` é necessário no momento ao usar o comando `rect=` com uma solicitação de imagem ou máscara.

## Diferenças conhecidas textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* O itálico sintético é renderizado menos inclinado do que ao usar `text=`.
* O sublinhado é um pouco mais baixo e mais fino do que ao usar `text=`.
* `\expnd` e  `\expndtw` usados com valores negativos altos fazem com que os caracteres sejam colocados na frente uns dos outros ao usar o  `text=`.

* `\charscaley` é dimensionada de forma diferente do que ao usar,  `text=` mas não afeta a altura da linha.

* Se a última linha de texto não se ajustar, a linha inteira será solta em vez de aparecer como recorte.
* `\slmult` e  `\sl` comportar-se de forma diferente do MS Word e  `text=`, apenas produzem efeitos relativamente aos parágrafos atuais e subsequentes.

* `\sb` aplica-se ao primeiro parágrafo tanto para o MS Word como para o  `text=`, o Adobe InDesign e o Photoshop não o fazem.

* `\sa` aplica-se ao último parágrafo para o MS Word e  `text=`, o Adobe InDesign e o Photoshop não fazem isso.

## Compatibilidade com versões anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapar o caractere sublinhado ( `\_`) em uma string RTF não funciona com todas as fontes usando `textPs=`

* Suporte ao tratamento de macro que não diferencia maiúsculas de minúsculas.
* O cache do catálogo foi reduzido de 60 segundos para 10 segundos.
* O recurso de redirecionamento de erro agora só redireciona solicitações que façam referência a imagens corrompidas, fontes, perfis de cores e imagens que são publicadas em um catálogo, mas não encontradas no disco.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=` e  `originN=` agora retornam um erro de análise se qualquer um dos valores do modificador for maior que 2147483648.

* Não há suporte para codificação de solicitações aninhadas. Transição para o novo comportamento e cancelamento da codificação de quaisquer valores de solicitação aninhados encontrados em solicitações de URL no seu site e nos catálogos da sua empresa.
* DefaultImage agora aplica atributos de miniatura ao usar `req=tmb`.
* Em versões anteriores usando `flip=`, a imagem nunca era reposicionada, independentemente do ponto de ancoragem.

## Restrições aplicáveis a bibliotecas de terceiros {#section-79768b96bf634e44ab672c5b893f343d}

A biblioteca Digimarc se recusa a aplicar uma marca d&#39;água Digimarc a uma imagem se ela já tiver sido detectada. Se uma edição suficiente for feita em uma imagem primária, a biblioteca Digimarc ainda poderá reconhecer que a marca d&#39;água foi aplicada. No entanto, pode não conseguir ler essas informações. Isso resulta em uma nova imagem na qual as informações originais da Digimarc que foram aplicadas à imagem original não podem ser obtidas. O Image Serving agora pode aplicar a marca d&#39;água Digimarc definida no catálogo da empresa.

## Restrições aplicáveis ao Serviço de imagem e à Renderização de imagem {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* O fornecimento de imagens e a renderização de imagens podem não aproveitar ao máximo todas as CPUs quando há mais de 4 CPUs disponíveis. Simule seu tráfego nessas máquinas para ver a sua vantagem com mais de 4 CPUs.
* URLs remotos que retornam um redirecionamento (status HTTP 301, 302 ou 303) são rejeitados.
* Ao configurar `errorRedirect.rootUrl` o endereço IP definido nessa propriedade precisa ser incluído no valor da tag do conjunto de regras `<addressfilter>` nesse servidor.

   *Exemplo*:

   O Servidor A definiu `errorRedirect.rootUrl=10.10.10.10` .

   O Servidor B, que tem o endereço IP 10.10.10.10, define o valor da tag `<addressfilter>` no arquivo do conjunto de regras para incluir seu endereço IP (10.10.10.10).

* O texto pontual e o caminho do texto com posicionamento podem exibir recorte.
* `text=` aplica-se somente  `\sa` e  `\sb` a todo o bloco de texto e não a cada parágrafo.

* Ao usar uma empresa definida no URL e outra empresa definida para o modificador `src=` ou `mask=`, é necessário prefixar uma barra para a empresa definida para `src=` ou `mask=` para que esse formulário de solicitação funcione.

   *Exemplo*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Em vez de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* As solicitações de Tiff ou vinheta sem Pirâmide geram uma mensagem de erro semelhante à de

   *&quot;A imagem não  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` tem DSF válido e a área de 2,25MPixel excede o máximo de 2MPixel&quot;* .

   A prática recomendada é usar arquivos virtuais e vinhetas em pirâmide. Se tiver de utilizar algemas ou vinhetas sem pirâmide, siga as instruções abaixo para aumentar o limite de tamanho.

   *Solução alternativa*:

   Para vinhetas sem pirâmide de renderização de imagem, aumente o valor da propriedade para IrMaxNonPyrVignetteSize no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Para TIFFs que não são de pirâmide do Serviço de imagem, aumente o valor da propriedade para `MaxNonDsfSize` no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* O Adobe Photoshop CS3 não salva arquivos PSD em camadas por padrão em uma imagem composta.

   *Sintomas*:

   O arquivo PSD em camadas do Adobe Photoshop CS3 é exibido em preto com texto informando: &quot;Esse arquivo Photoshop em camadas não foi salvo com uma imagem composta&quot;. para a imagem de resposta do Image Serving ou no IPS.

   *Solução alternativa*:

   Salve o arquivo Adobe Photoshop CS3 com o máximo de compatibilidade ativado.

* Atribuir o perfil ICC a uma imagem de resposta CMYK/JPEG faz com que as cores sejam invertidas em alguns navegadores.*Solução alternativa*:

   Altere o formato da imagem de resposta usando `fmt=`

* O tamanho da imagem de resposta HTTP data-after de compactação, incluindo cabeçalho de arquivo-é limitado a 16 MB.
* &quot; ..&quot; não é permitido em nenhum elemento de caminho em solicitações HTTP.
* A desinstalação pode remover o arquivo criado ou modificado pelo usuário de *[!DNL install_root]* ou qualquer subpasta. Copie esses arquivos para um local diferente antes de desinstalar.

## Restrições aplicáveis somente ao Serviço de imagem {#section-b08ad535e4454265b8157dec244c4faf}

* As cores do primeiro plano no comando RTF ( `\cf`) não são compatíveis com o texto PhotoFont.
* A sintetização de negrito, itálico e negrito/itálico será rejeitada como um erro para o texto do PhotoFont.
* O fluxo de texto vertical não é compatível com o texto PhotoFont.
* Imagens PNG de 16bpc não são compatíveis com texto PhotoFont.
* As correções de cores para imagens PNG com perfis de cores incorporados usam opções codificadas. A intenção de renderização é colorimétrica relativa e a compensação de ponto preto está ativada para o texto da fonte de foto.
* A pesquisa baseada em arquivo não é suportada quando a tradução local está ativada no arquivo [!DNL ini] da empresa.
* O Serviço de imagem não grava caminhos Photoshop não fechados corretamente.
* No momento, a Exibição de imagem não suporta o processamento de arquivos TIFF exportados usando o Adobe Media Encoder 4.0.1 ou anterior. O Adobe Media Encoder está incluído no Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* Usar `text=` com camadas de dimensionamento automático não suporta cadeias de caracteres RTF que usam mais de uma configuração para justificação de linha.

   *Exemplo*

   A sequência de caracteres RTF não pode usar a justificação da linha esquerda e direita para uma camada de texto de autodimensionamento.

* O SVG tem sua própria propriedade para o caminho de pesquisa de fonte das fontes referenciadas que não estão incorporadas ao arquivo SVG.

   *Sintomas*

   Imagens SVG renderizadas que contêm definições de fonte estão usando a fonte incorreta.

   *Solução alternativa*

   Defina a propriedade `svgProvider.fontRoot=` em [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* O Recorte está usando `bgColor=` no momento, em vez de `color=` para preencher qualquer área recém-estendida.

* A conversão de cores pode não estar correta quando `bgColor=` não corresponde ao espaço de cores base que envolve perfis de cores.
* Os efeitos da camada externa não são renderizados se a camada não tiver uma máscara ou dados alfa.

## Restrições aplicáveis somente à Renderização de imagem {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Os decalques e materiais de parede não podem ser removidos.
* O tamanho das texturas é limitado em relação ao tamanho da exibição da vinheta. Em raras circunstâncias, o limite padrão de 425% do tamanho de exibição pode interferir em um aplicativo usando texturas não repetitivas muito grandes. Se não for possível alterar o aplicativo ou o conteúdo para funcionar dentro das limitações predefinidas, a porcentagem pode ser aumentada da seguinte maneira. Usando um editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localize `IrMaxTextureSizeFactor` e insira um novo valor de porcentagem. A alteração entrará em vigor imediatamente sem reiniciar o Servidor de imagem.

* Os mecanismos JavaScript nos dados de resposta do cache do Netscape e Opera, mesmo se o cabeçalho nocache estiver definido. Isso interfere no bom funcionamento dos pedidos de Estado.

   *Solução alternativa*

   Anexe um carimbo de data e hora ou outro identificador exclusivo à cadeia de caracteres da solicitação, como `"&.ts=currentTime`.

## Restrições aplicáveis somente a utilitários {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`às vezes falha com uma falha de segmentação quando parada com um  `control-c`.
