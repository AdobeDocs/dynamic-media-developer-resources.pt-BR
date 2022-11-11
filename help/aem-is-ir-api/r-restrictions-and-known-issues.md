---
description: Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.
solution: Experience Manager
title: Restrições e problemas conhecidos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# Restrições e problemas conhecidos{#restrictions-and-known-issues}

Há algumas restrições e problemas conhecidos que devem ser considerados ao usar o Dynamic Media Image Serving.

## Erata da documentação {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* O número de linhas não excederá o máximo de `\copyfitmaxlines` e o número de linhas explícitas na entrada de texto.
* São necessários parênteses e colchetes correspondentes em conjuntos de imagens. Se as chaves e os parênteses não corresponderem, eles precisarão ser codificados no URL.
* O alerta de tempo de resposta global do lado do servidor inclui respostas de erro.
* O `id=` no momento, é necessário usar o comando `rect=` com uma solicitação de imagem ou máscara.

## Diferenças conhecidas textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* O itálico sintético é renderizado menos inclinado do que ao usar `text=`.
* O sublinhado é um pouco mais baixo e mais fino do que ao usar `text=`.
* `\expnd` e `\expndtw` usados com valores negativos altos fazem com que os caracteres sejam colocados na frente um do outro ao usar `text=`.

* `\charscaley` escalas diferentes de quando usar `text=` mas não afeta a altura da linha.

* Se a última linha de texto não se ajustar, a linha inteira será solta em vez de aparecer como recorte.
* `\slmult` e `\sl` comportar-se de forma diferente do MS Word e `text=`, apenas produzirão efeitos para os parágrafos atuais e subsequentes.

* `\sb` aplica-se ao primeiro parágrafo tanto para o MS Word como para o `text=`, Adobe InDesign e [!DNL Photoshop] não faça isso.

* `\sa` aplica-se ao último parágrafo para o MS Word e `text=`, Adobe InDesign e [!DNL Photoshop] não faça isso.

## Compatibilidade com versões anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapando o caractere sublinhado ( `\_`) em uma string RTF não funciona com todas as fontes que usam `textPs=`

* Suporte ao tratamento de macro que não diferencia maiúsculas de minúsculas.
* O cache do catálogo foi reduzido de 60 segundos para 10 segundos.
* O recurso de redirecionamento de erro agora só redireciona solicitações que façam referência a imagens corrompidas, fontes, perfis de cores e imagens que são publicadas em um catálogo, mas não encontradas no disco.
* `posN=`, `anchor=`, `anchorN=`, `origin=`e `originN=` agora retorna um erro de análise se qualquer um dos valores do modificador for maior que 2147483648.

* Não há suporte para codificação de solicitações aninhadas. Transição para o novo comportamento e cancelamento da codificação de quaisquer valores de solicitação aninhados encontrados em solicitações de URL do seu site e em catálogos da sua empresa.
* O DefaultImage agora aplica atributos de miniatura ao usar `req=tmb`.
* Em versões anteriores que usavam `flip=`, a imagem nunca foi reposicionada, independentemente do ponto de ancoragem.

## Restrições aplicáveis a bibliotecas de terceiros {#section-79768b96bf634e44ab672c5b893f343d}

A biblioteca Digimarc se recusa a aplicar uma marca d&#39;água Digimarc a uma imagem se ela já tiver sido detectada. Se uma edição suficiente for feita em uma imagem primária, a biblioteca Digimarc ainda poderá reconhecer que a marca d&#39;água foi aplicada. No entanto, pode não conseguir ler essas informações. Isso resulta em uma nova imagem na qual as informações originais da Digimarc que foram aplicadas à imagem original não podem ser obtidas. O Image Serving agora pode aplicar a marca d&#39;água Digimarc definida no catálogo da empresa.

## Restrições aplicáveis ao fornecimento de imagens e à renderização de imagens {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* O fornecimento de imagens e a renderização de imagens podem não aproveitar ao máximo todas as CPUs quando há mais de 4 CPUs disponíveis. Simule seu tráfego nessas máquinas para ver a sua vantagem com mais de 4 CPUs.
* URLs remotos que retornam um redirecionamento (status HTTP 301, 302 ou 303) são rejeitados.
* Ao configurar `errorRedirect.rootUrl` o endereço IP definido nessa propriedade precisa ser incluído no conjunto de regras `<addressfilter>` valor da tag nesse servidor.

   *Exemplo*:

   O servidor A foi definido `errorRedirect.rootUrl=10.10.10.10` .

   O Servidor B, que tem o endereço IP 10.10.10.10, define o `<addressfilter>` no arquivo do conjunto de regras para incluir seu endereço IP (10.10.10.10).

* O texto pontual e o caminho do texto com posicionamento podem exibir recorte.
* `text=` só se aplica `\sa` e `\sb` ao bloco de texto inteiro e não por parágrafo.

* Ao usar uma empresa definida no URL e outra empresa definida para a `src=` ou `mask=` modificador, é necessário prefixar uma barra para a empresa definida para `src=` ou `mask=` para que esta forma de solicitação funcione.

   *Exemplo*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Em vez de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* As solicitações de Tiff ou vinheta sem Pirâmide geram uma mensagem de erro semelhante à de

   *&quot;Imagem `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` não tem DSF válido e a área de 2,25MPixel excede o máximo de 2 MPixel&quot;* .

   A prática recomendada é usar arquivos virtuais e vinhetas em pirâmide. Se tiver de utilizar algemas ou vinhetas sem pirâmide, siga as instruções abaixo para aumentar o limite de tamanho.

   *Solução alternativa*:

   Para vinhetas não-pirâmides de Renderização de Imagem, aumente o valor da propriedade para IrMaxNonPyrVignetteSize no [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] arquivo de configuração.

   Para TIFF não-pirâmide do Image Serving, aumente o valor da propriedade de `MaxNonDsfSize` no [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] arquivo de configuração.

* Adobe [!DNL Photoshop] O CS3 não salva arquivos PSD em camadas por padrão em uma imagem composta.

   *Sintomas*:

   O Adobe [!DNL Photoshop] O arquivo de PSD em camadas CS3 é exibido em preto com texto informando: &quot;Este arquivo em camadas [!DNL Photoshop] não foi salvo com uma imagem composta.&quot; para a imagem de resposta do Image Serving ou no IPS.

   *Solução alternativa*:

   Salve o Adobe [!DNL Photoshop] Arquivo CS3 com compatibilidade máxima ativada.

* Atribuir o perfil ICC a uma imagem de resposta CMYK/JPEG faz com que as cores sejam invertidas em alguns navegadores.*Solução alternativa*:

   Alterar o formato da imagem de resposta usando `fmt=`

* O tamanho da imagem de resposta HTTP data-after de compactação, incluindo cabeçalho de arquivo-é limitado a 16 MB.
* &quot; ..&quot; não é permitido em nenhum elemento de caminho em solicitações HTTP.
* A desinstalação pode remover o arquivo criado ou modificado pelo usuário do *[!DNL install_root]* ou qualquer subpasta. Copie esses arquivos para um local diferente antes de desinstalar.

## Restrições aplicáveis somente ao fornecimento de imagens {#section-b08ad535e4454265b8157dec244c4faf}

* Cores do primeiro plano no RTF ( `\cf`) não são compatíveis com o texto PhotoFont.
* A síntese de negrito, itálico e negrito/itálico é rejeitada como um erro para o texto do PhotoFont.
* O fluxo de texto vertical não é compatível com o texto PhotoFont.
* Imagens PNG de 16bpc não são compatíveis com texto PhotoFont.
* As correções de cores para imagens PNG com perfis de cores incorporados usam opções codificadas. A intenção de renderização é colorimétrica relativa e a compensação de ponto preto está ativada para o texto da fonte de foto.
* A pesquisa baseada em arquivo não é suportada quando a tradução local está ativada na empresa [!DNL ini] arquivo.
* O Serviço de Imagens não grava não fechado [!DNL Photoshop] caminhos corretamente.
* No momento, a exibição de imagens não suporta o processamento de arquivos TIFF exportados usando o Adobe Media Encoder 4.0.1 ou anterior. O Adobe Media Encoder está incluído no Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* Usando `text=` com camadas de dimensionamento automático não suporta cadeias de caracteres RTF que usam mais de uma configuração para justificação de linha.

   *Exemplo*

   A sequência de caracteres RTF não pode usar a justificação da linha esquerda e direita para uma camada de texto de autodimensionamento.

* O SVG tem sua própria propriedade para o caminho de pesquisa de fonte das fontes referenciadas que não estão incorporadas no arquivo SVG.

   *Sintomas*

   Imagens SVG renderizadas que contêm definições de fonte estão usando a fonte incorreta.

   *Solução alternativa*

   Definir a propriedade `svgProvider.fontRoot=` em [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Cortar está usando `bgColor=` em vez de `color=` para preencher qualquer área recentemente alargada.

* A conversão de cor pode não estar correta quando `bgColor=` não corresponde ao espaço de cores base que envolve perfis de cores.
* Os efeitos da camada externa não são renderizados se a camada não tiver uma máscara ou dados alfa.

## Restrições aplicáveis somente à renderização de imagens {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Os decalques e materiais de parede não podem ser removidos.
* O tamanho das texturas é limitado em relação ao tamanho da exibição da vinheta. Em raras circunstâncias, o limite padrão de 425% do tamanho de exibição pode interferir em um aplicativo usando texturas não repetitivas muito grandes. Se não for possível alterar o aplicativo ou o conteúdo para funcionar dentro das limitações predefinidas, a porcentagem pode ser aumentada da seguinte maneira. Usando um editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localizar `IrMaxTextureSizeFactor` e insira um novo valor de porcentagem. A alteração entrará em vigor imediatamente sem reiniciar o Servidor de imagem.

* Os mecanismos JavaScript nos dados de resposta do cache do Netscape e Opera, mesmo se o cabeçalho nocache estiver definido. Isso interfere no bom funcionamento dos pedidos de Estado.

   *Solução alternativa*

   Anexe um carimbo de data e hora ou outro identificador exclusivo à cadeia de caracteres de solicitação, como `"&.ts=currentTime`.

## Restrições aplicáveis apenas a serviços de utilidade pública {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`às vezes falha com uma falha de segmentação quando parada com um `control-c`.
