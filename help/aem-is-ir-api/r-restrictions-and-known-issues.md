---
description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.
solution: Experience Manager
title: Restrições e problemas conhecidos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# Restrições e problemas conhecidos{#restrictions-and-known-issues}

Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.

## Errata da documentação {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* O número de linhas não excede o máximo da configuração `\copyfitmaxlines` e o número de linhas explícitas na entrada de texto.
* As chaves e os parênteses correspondentes são necessários nos conjuntos de imagens. Se as chaves e os parênteses não corresponderem, eles precisarão ser codificados por URL.
* O alerta de tempo de resposta global do lado do servidor inclui respostas de erro.
* O comando `id=` é necessário no momento ao usar o comando `rect=` com uma solicitação de imagem ou máscara.

## Diferenças conhecidas textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* O itálico sintético é renderizado menos inclinado do que ao usar `text=`.
* O sublinhado é um pouco mais baixo e mais fino do que ao usar o `text=`.
* `\expnd` e `\expndtw` usados com valores negativos altos fazem com que os caracteres sejam colocados na frente um do outro ao usar `text=`.

* `\charscaley` é dimensionado de forma diferente ao usar `text=`, mas não afeta a altura da linha.

* Se a última linha de texto não couber, a linha inteira será solta em vez de aparecer como corte.
* `\slmult` e `\sl` se comportam de maneira diferente do MS Word e do `text=`, simplesmente fazem efeito para os parágrafos atuais e subsequentes.

* `\sb` se aplica ao primeiro parágrafo para o MS Word e `text=`, Adobe InDesign e [!DNL Photoshop] não fazem isso.

* `\sa` se aplica ao último parágrafo para o MS Word e `text=`, Adobe InDesign e [!DNL Photoshop] não fazem isso.

## Compatibilidade com versões anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapar o caractere de sublinhado ( `\_`) em uma cadeia de caracteres RTF não funciona com todas as fontes que usam `textPs=`

* Suporte para manipulação de macros que não diferenciam maiúsculas de minúsculas.
* O cache do catálogo foi reduzido de 60 segundos para 10 segundos.
* O recurso de redirecionamento de erro agora apenas redireciona solicitações referenciando imagens, fontes, perfis de cores e imagens corrompidas publicadas em um catálogo, mas não encontradas no disco.
* `posN=`, `anchor=`, `anchorN=`, `origin=` e `originN=` agora retornam um erro de análise se qualquer um dos valores do modificador for maior que 2147483648.

* Não há suporte para a codificação de solicitações aninhadas. Faça a transição para o novo comportamento e decodifique quaisquer valores de solicitação aninhados encontrados em solicitações de URL no seu site e nos catálogos da sua empresa.
* DefaultImage agora aplica atributos de miniatura ao usar `req=tmb`.
* Em versões anteriores que usavam `flip=`, a imagem nunca era reposicionada independentemente do ponto de ancoragem.

## Restrições aplicáveis a bibliotecas de terceiros {#section-79768b96bf634e44ab672c5b893f343d}

A biblioteca da Digimarc se recusa a aplicar uma marca d&#39;água da Digimarc a uma imagem, se ela já tiver sido detectada. Se uma edição suficiente for feita em uma imagem principal, a biblioteca Digimarc ainda poderá reconhecer que a marca d&#39;água foi aplicada. No entanto, pode não ser capaz de ler essas informações. Isso resulta em uma nova imagem em que as informações originais da Digimarc aplicadas à imagem original não podem ser obtidas. O Servidor de imagens agora pode aplicar a marca d&#39;água da Digimarc definida no catálogo da empresa.

## Restrições aplicáveis ao Servidor de imagens e à Renderização de imagens {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* O Servidor de imagens e a Renderização de imagens podem não aproveitar totalmente todas as CPUs quando houver mais de 4 CPUs disponíveis. Simule seu tráfego nessas máquinas para ver o quanto ele é vantajoso com mais de 4 CPUs.
* Os URLs remotos que retornam um redirecionamento (status HTTP 301, 302 ou 303) são rejeitados.
* Ao configurar `errorRedirect.rootUrl`, o endereço IP definido nessa propriedade precisa ser incluído no valor da marca do conjunto de regras `<addressfilter>` nesse servidor.

  *Exemplo*:

  O servidor A definiu `errorRedirect.rootUrl=10.10.10.10`.

  O Servidor B, que tem o endereço IP 10.10.10.10, define o valor da marca `<addressfilter>` no arquivo de conjunto de regras para incluir seu endereço IP (10.10.10.10).

* O texto de ponto e o caminho de texto com posicionamento podem exibir recorte.
* `text=` aplica somente `\sa` e `\sb` ao bloco de texto inteiro e não por parágrafo.

* Ao usar uma empresa definida na URL e outra empresa definida para o modificador `src=` ou `mask=`, você deve prefixar uma barra à empresa definida para `src=` ou `mask=` para que esta forma de solicitação funcione.

  *Exemplo*:

  `/is/image/MyCompany?src=/YourCompany/MyImage`.

  Em vez de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* As solicitações de Tiff ou vinheta não piramidadas produzem uma mensagem de erro semelhante a

  *&quot;A imagem `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` não tem DSF válido e a área de 2,25 MPixel excede o máximo de 2 MPixel&quot;* .

  A prática recomendada é usar Tiffs e vinhetas em pirâmide. Se tiver necessidade de utilizar dispositivos de segurança ou vinhetas não piramidadas, siga as instruções abaixo para aumentar o limite de tamanho.

  *Solução alternativa*:

  Para Renderização de Imagem de vinhetas não piramidadas, aumente o valor da propriedade para IrMaxNonPyrVignetteSize no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

  Para TIFF não piramidados do Servidor de imagens, aumente o valor da propriedade para `MaxNonDsfSize` no arquivo de configuração [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* O Adobe [!DNL Photoshop] CS3 não salva arquivos PSD em camadas como uma imagem composta por padrão.

  *Sintomas*:

  O arquivo de PSD em camadas Adobe [!DNL Photoshop] CS3 é exibido em preto com texto declarando: &quot;Este arquivo [!DNL Photoshop] em camadas não foi salvo com uma imagem composta.&quot; para a imagem de resposta do Servidor de imagens ou no IPS.

  *Solução alternativa*:

  Salve o arquivo Adobe [!DNL Photoshop] CS3 com a opção maximizar compatibilidade ativada.

* Atribuir um perfil ICC a uma imagem de resposta CMYK/JPEG faz com que as cores sejam invertidas em alguns navegadores.*Solução alternativa*:

  Alterar formato da imagem de resposta usando `fmt=`

* O tamanho dos dados da imagem de resposta HTTP após a compactação, incluindo o cabeçalho do arquivo, é limitado a 16 MB.
* &quot; ..&quot; não é permitido em nenhum elemento de caminho em solicitações HTTP.
* A desinstalação pode remover arquivos criados ou modificados pelo usuário de *[!DNL install_root]* ou de qualquer subpasta. Copie esses arquivos para um local diferente antes de desinstalar.

## Restrições aplicáveis apenas ao Servidor de imagens {#section-b08ad535e4454265b8157dec244c4faf}

* Não há suporte para cores de primeiro plano no comando RTF ( `\cf`) para texto PhotoFont.
* A síntese de negrito, itálico e negrito/itálico é rejeitada como um erro para o texto PhotoFont.
* O fluxo de texto vertical não é suportado para texto PhotoFont.
* Imagens PNG de 16bpc não são compatíveis com texto PhotoFont.
* As correções de cores para imagens PNG com perfis de cores incorporados usam opções embutidas em código. A intenção de renderização é colorimétrica relativa e a compensação de Blackpoint está ativada para o texto PhotoFont.
* Não há suporte para a pesquisa baseada em arquivo quando a conversão de localidade está habilitada no arquivo da empresa [!DNL ini].
* O Servidor de imagens não grava corretamente caminhos [!DNL Photoshop] não fechados.
* No momento, o Servidor de imagens não oferece suporte ao processamento de arquivos TIFF exportados com o Adobe Media Encoder 4.0.1 ou anterior. A Adobe Media Encoder está incluída no Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* O uso de `text=` com camadas de autodimensionamento não oferece suporte a cadeias de caracteres RTF que usam mais de uma configuração para justificação de linha.

  *Exemplo*

  A cadeia de caracteres RTF não pode usar justificativas de linha esquerda e direita para uma camada de texto de autodimensionamento.

* O SVG tem sua própria propriedade para o caminho de pesquisa de fontes referenciadas que não estão incorporadas no arquivo SVG.

  *Sintomas*

  Imagens de SVG renderizadas que contêm definições de fonte estão usando a fonte incorreta.

  *Solução alternativa*

  Defina a propriedade `svgProvider.fontRoot=` em [!DNL install_root/ImageServing/conf/PlatformServer.conf].

* O recorte está usando `bgColor=` em vez de `color=` para preencher qualquer área estendida recentemente.

* A conversão de cores pode não estar correta quando `bgColor=` não corresponde ao espaço de cores de base que envolve perfis de cores.
* Os efeitos de camada externa não são renderizados se a camada não tiver uma máscara ou dados alfa.

## Restrições aplicáveis somente à renderização de imagem {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decalques e materiais de parede não são removíveis.
* O tamanho das texturas é limitado em relação ao tamanho da exibição de vinheta. Em raras circunstâncias, o limite padrão de 425% do tamanho da exibição pode interferir em um aplicativo que usa texturas muito grandes não repetíveis. Se não for possível alterar o aplicativo ou o conteúdo para funcionar dentro das limitações predefinidas, a porcentagem poderá ser aumentada da seguinte maneira. Usando um editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localize `IrMaxTextureSizeFactor` e insira um novo valor de porcentagem. A alteração entra em vigor imediatamente sem reiniciar o Servidor de imagens.

* Os mecanismos do JavaScript nos dados de resposta do cache do Netscape e Opera, mesmo que o cabeçalho nocache esteja definido. Isso interfere no funcionamento correto de solicitações com informações de estado.

  *Solução alternativa*

  Anexe um carimbo de data e hora ou outro identificador exclusivo à cadeia de caracteres da solicitação, como `"&.ts=currentTime`.

## Restrições aplicáveis apenas a serviços públicos {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`às vezes trava com uma falha de segmentação quando parado com um `control-c`.
