---
description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Server.
seo-description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Server.
seo-title: Restrições e problemas conhecidos
solution: Experience Manager
title: Restrições e problemas conhecidos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Restrições e problemas conhecidos{#restrictions-and-known-issues}

Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Server.

## Documentação errata {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* O número de linhas não excederá o máximo da configuração `\copyfitmaxlines` e o número de linhas explícitas na entrada de texto.
* São necessários parênteses e chaves correspondentes em conjuntos de imagens. Se as chaves e os parênteses não forem correspondentes, eles precisarão ser codificados no URL.
* O alerta de tempo de resposta global do servidor inclui respostas de erro.
* O comando `id=` é necessário no momento ao usar o comando `rect=` com uma solicitação de imagem ou máscara.

## Diferenças conhecidas textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* O itálico sintético é renderizado com menos inclinação do que ao usar `text=`.
* O sublinhado é um pouco mais baixo e mais fino do que ao usar `text=`.
* `\expnd` e  `\expndtw` usados com valores negativos altos fazem com que os caracteres sejam colocados na frente uns dos outros ao usar  `text=`.

* `\charscaley` dimensiona de forma diferente do que ao usar,  `text=` mas não afeta a altura da linha.

* Se a última linha de texto não se ajustar, a linha inteira será solta em vez de aparecer como corte.
* `\slmult` e  `\sl` comportam-se de forma diferente do MS Word e  `text=`, simplesmente entram em vigor para os parágrafos atuais e posteriores.

* `\sb` se aplica ao primeiro parágrafo para MS Word e  `text=`, Adobe InDesign e Photoshop não fazem isso.

* `\sa` se aplica ao último parágrafo para MS Word e  `text=`, Adobe InDesign e Photoshop não fazem isso.

## Compatibilidade com versões anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapar o caractere sublinhado ( `\_`) em uma string RTF não funciona com todas as fontes usando `textPs=`

* Suporte para manipulação de macro sem distinção entre maiúsculas e minúsculas.
* O cache do catálogo foi reduzido de 60 para 10 segundos.
* O recurso de redirecionamento de erro agora redireciona somente as solicitações que fazem referência a imagens corrompidas, fontes, perfis coloridos e imagens publicadas em um catálogo, mas não encontradas em disco.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=`e  `originN=` agora retorna um erro de análise se qualquer um dos valores do modificador for maior que 2147483648.

* A codificação de solicitações aninhadas não é suportada. Transição ao novo comportamento e descodifique quaisquer valores de solicitação aninhados encontrados em solicitações de URL no seu site e em seus catálogos de empresa.
* DefaultImage agora aplica atributos de miniatura ao usar `req=tmb`.
* Em versões anteriores usando `flip=`, a imagem nunca foi reposicionada independentemente do ponto de ancoragem.

## Restrições aplicáveis a bibliotecas de terceiros {#section-79768b96bf634e44ab672c5b893f343d}

A biblioteca Digimarc se recusa a aplicar uma marca d&#39;água Digimarc a uma imagem se ela já tiver sido detectada. Se uma edição suficiente for feita em uma imagem primária, a biblioteca Digimarc ainda poderá reconhecer que a marca d&#39;água foi aplicada. No entanto, pode não ser capaz de ler essa informação. Isso resulta em uma nova imagem na qual as informações originais da Digimarc aplicadas à imagem original não podem ser obtidas. O Serviço de imagem agora pode aplicar a marca d&#39;água Digimarc definida no catálogo de empresas.

## Restrições aplicáveis ao Serviço de imagem e à Renderização de imagem {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* O serviço de imagem e a renderização de imagem podem não aproveitar todas as CPUs quando há mais de 4 CPUs disponíveis. Simule seu tráfego nesses computadores para ver a sua vantagem com mais de 4 CPUs.
* URLs remotos que retornam um redirecionamento (status HTTP 301, 302 ou 303) são rejeitados.
* Ao configurar `errorRedirect.rootUrl`, o endereço IP definido nesta propriedade precisa ser incluído no valor da tag `<addressfilter>` do conjunto de regras nesse servidor.

   *Exemplo*:

   O servidor A definiu `errorRedirect.rootUrl=10.10.10.10`.

   O servidor B, que tem o endereço IP 10.10.10.10, define o valor da tag `<addressfilter>` no arquivo de conjunto de regras para incluir seu endereço IP (10.10.10.10).

* O texto do ponto e o caminho do texto com posicionamento podem exibir recorte.
* `text=` aplica-se somente  `\sa` e  `\sb` a todo o bloco de texto e não a cada parágrafo.

* Ao usar uma empresa definida no URL e outra empresa definida para o modificador `src=` ou `mask=`, você deve prefixar uma barra para a empresa definida para `src=` ou `mask=` para que esse formulário de solicitação funcione.

   *Exemplo*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Em vez de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* As solicitações de TIFF ou vinheta sem pirâmide geram uma mensagem de erro semelhante à

   *&quot;A imagem não  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` tem um DSF válido e a área de 2,25MPixel excede o máximo de 2 MPixel&quot;* .

   A melhor prática é usar arquivos em pirâmide e vinhetas. Se tiver de utilizar pontas ou vinhetas não pirâmides, siga as instruções abaixo para aumentar o limite de tamanho.

   *Solução*:

   Para renderizar vinhetas não pirâmides, aumente o valor da propriedade para IrMaxNonPyrVignetteSize no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Para TIFFs sem pirâmide do Serviço de imagem, aumente o valor da propriedade para `MaxNonDsfSize` no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* O Adobe Photoshop CS3 não salva arquivos PSD em camadas por padrão em uma imagem composta.

   *Sintomas*:

   O arquivo PSD em camadas do Adobe Photoshop CS3 é exibido como preto com o texto informando: &quot;Esse arquivo Photoshop em camadas não foi salvo com uma imagem composta.&quot; para a imagem de resposta do Servidor de imagens ou no IPS.

   *Solução*:

   Salve o arquivo Adobe Photoshop CS3 com o máximo de compatibilidade ativado.

* Atribuir Perfil ICC a uma imagem de resposta CMYK/JPEG faz com que as cores sejam invertidas em alguns navegadores.*Solução*:

   Altere o formato da imagem de resposta usando `fmt=`

* O tamanho da imagem de resposta HTTP após a compactação, incluindo o cabeçalho do arquivo, é limitado a 16 MB.
* &quot; ..&quot; não é permitido em nenhum elemento de caminho em solicitações HTTP.
* A desinstalação pode remover arquivos criados pelo usuário ou modificados de *[!DNL install_root]* ou de qualquer subpasta. Copie esses arquivos para um local diferente antes de desinstalar.

## Restrições aplicáveis somente ao Serviço de Imagem {#section-b08ad535e4454265b8157dec244c4faf}

* As cores de primeiro plano no comando RTF ( `\cf`) não são compatíveis com o texto PhotoFont.
* A síntese de negrito, itálico e negrito/itálico será rejeitada como um erro para o texto PhotoFont.
* O fluxo de texto vertical não é compatível com o texto PhotoFont.
* Imagens PNG de 16bpc não são compatíveis com texto PhotoFont.
* As correções de cores para imagens PNG com perfis de cor incorporados usam opções codificadas. O propósito de renderização é colorimétrico relativo e a compensação do ponto preto está ativada para o texto PhotoFont.
* A pesquisa baseada em arquivo não é suportada quando a tradução de localidade está ativada no arquivo [!DNL ini] da empresa.
* O Serviço de imagem não grava corretamente caminhos Photoshop não fechados.
* No momento, o Serviço de imagem não oferece suporte ao processamento de arquivos TIFF exportados usando o Adobe Media Encoder 4.0.1 ou anterior. A Adobe Media Encoder está incluída no Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* Usar `text=` com camadas de autodimensionamento não suporta strings RTF que usam mais de uma configuração para a justificação de linha.

   *Exemplo*

   A string RTF não pode usar a justificação de linha esquerda e direita para uma camada de texto de autodimensionamento.

* O SVG tem sua própria propriedade para o caminho de pesquisa de fonte das fontes referenciadas que não estão incorporadas no arquivo SVG.

   *Sintomas*

   As imagens SVG renderizadas que contêm definições de fonte estão usando a fonte incorreta.

   *Solução*

   Defina a propriedade `svgProvider.fontRoot=` em [!DNL install_root/ImageServing/conf/PlatformServer.conf].

* Atualmente, a opção Recortar está usando `bgColor=` em vez de `color=` para preencher qualquer área recentemente estendida.

* A conversão de cores pode não estar correta quando `bgColor=` não corresponde ao espaço de cores base que envolve perfis de cores.
* Os efeitos de camada externa não são renderizados se a camada não tiver uma máscara ou dados alfa.

## Restrições aplicáveis somente à renderização de imagem {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Os decalques e materiais de parede não são removíveis.
* O tamanho das texturas é limitado em relação ao tamanho da visualização da vinheta. Em raras circunstâncias, o limite padrão de 425% do tamanho da visualização pode interferir com um aplicativo usando texturas muito grandes não repetíveis. Se não for possível alterar o aplicativo ou o conteúdo para que funcione dentro das limitações predefinidas, a porcentagem pode ser aumentada da seguinte forma. Usando um editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localize `IrMaxTextureSizeFactor` e insira um novo valor de porcentagem. A alteração entrará em vigor imediatamente sem reiniciar o Servidor de imagens.

* Os mecanismos JavaScript nos dados de resposta do cache Netscape e Opera mesmo se o cabeçalho nocache estiver definido. Isto interfere no funcionamento adequado dos pedidos de Estado.

   *Solução*

   Anexe um carimbo de data e hora ou outro identificador exclusivo à string de solicitação, como `"&.ts=currentTime`.

## Restrições aplicáveis somente a utilitários {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`às vezes falha com uma falha de segmentação quando parada com um  `control-c`.
