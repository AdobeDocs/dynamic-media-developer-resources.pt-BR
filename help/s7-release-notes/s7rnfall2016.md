---
description: '"As notas de versão mais recentes da versão do último trimestre de 2016 da Adobe Scene7, parte da solução Adobe Experience Manager na Adobe Marketing Cloud."'
solution: Experience Manager
title: Versão do último trimestre de 2016 do Scene7
feature: Dynamic Media Classic
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2238'
ht-degree: 0%

---


# Versão do último trimestre de 2016 do Scene7{#scene-fall-release}

As notas de versão mais recentes para a parte de versão do último trimestre de 2016 da Adobe Scene7 da solução Adobe Experience Manager na Adobe Marketing Cloud.

## Versão do último trimestre de 2016 do Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

As notas de versão mais recentes para a [!DNL Adobe Scene7] versão do último trimestre de 2016 da solução [!DNL Adobe Experience Manager] no [!DNL Adobe Marketing Cloud].

* [Geral](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizadores (Serviço de imagem 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizadores (Serviço de imagem 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizadores (Serviço de imagem 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [SDK do visualizador HTML5 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Geral {#section-52afeb72ecb34c1585ea67a5051825a2}

O Adobe está animado em anunciar a disponibilidade da entrega de conteúdo HTTP/2 com o benefício geral de melhor desempenho.

Consulte [Perguntas frequentes sobre entrega de conteúdo HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Sistema de publicação do Scene7 {#section-24487cb493444d808fb7193f0a00cdd4}

Para obter a documentação completa, consulte [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Novos recursos, melhorias e correções de erros**

* Remoção do recurso de recuperação de vídeo da interface do usuário [!DNL Adobe Scene7 Publishing System].
* Autenticação adicionada a todos os servlets Scene7, quando necessário e possível.
* Correção de erros envolvendo a Exibição de lista na Lixeira.
* Remoção do recurso de usuário **Criar administrador do Dynamic Media Classic (Scene7)** do Gerenciamento de usuários devido a questões de segurança.
* O FTP WebAdmin agora é compatível com a autenticação OKTA.
* Remoção do recurso da senha padrão que foi criada para novos usuários do Media Portal.
* Correção de erros envolvendo a senha temporária gerada quando um novo usuário foi adicionado. A senha não atendeu aos requisitos necessários de senha.
* Solução de problemas completos do disco raiz do WebAdmin.
* Correção de erros que envolvia a desativação de um usuário não sendo refletida imediatamente na interface do usuário.
* Correção de erros envolvendo a exclusão de um usuário que não permitiu recriar o usuário posteriormente.
* Correção de erros envolvendo o email de boas-vindas enviado para novos usuários do Scene7 que não incluíam autenticação para controlar determinadas configurações.
* Correção de erros envolvendo a falha na recuperação de uma lista de pastas FTP se qualquer pasta tiver caracteres especiais em seu nome.
* Configurar provedores de serviço OKTA para ambientes Scene7.
* Adição de suporte à ID de organização do Marketing Cloud para o Viewer Analytics.
* Consumidor Scene7 SAML implementado.

## Visualizadores (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obter a documentação completa, consulte o [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correções de erros do Image Serving 5.5.3**

* Compatibilidade com as bibliotecas RequireJS e DOJO.

   Cache JS do SDK consolidado durante a implantação do visualizador.

## Visualizadores (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obter a documentação completa, consulte o [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correções de erros do Image Serving 5.5.2**

* Falha na reprodução do vídeo no Internet Explorer 11 no Windows 7.
* `initialframe` O não estava afetando o modo retrato em dispositivos móveis para o eCatalog HTML5.

## Visualizadores (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obter a documentação completa, consulte o [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Novos recursos, aprimoramentos e correções de erros do Image Serving 5.5.1**

* Visualizador de eCatalog do HTML5 com recurso de pesquisa.
* Adição da reprodução de vídeo de streaming HLS como método de entrega de vídeo padrão para a maioria dos sistemas de desktop. O streaming de vídeo HDS baseado em Flash ainda está disponível como uma opção de reprodução alternativa.
* Adição de suporte para dispositivos com entrada de mouse e toque executando o navegador Chrome.
* Adição do suporte à ID de organização do Marketing Cloud à integração do Analytics.
* Atualize a biblioteca do JavaScript do AppMeasurement para a versão 1.6.1.
* Adição de suporte para orientação da direita para a esquerda no visualizador do Catálogo eletrônico.
* Correção de um problema em que `tip=0,-1,0` causava um erro fora do intervalo.

**Notas de compatibilidade**

* BlackBerry

   * Incompatibilidade com conjuntos AVS mais antigos. Os clientes podem precisar fazer o upload novamente dos conjuntos de AVS para permitir a reprodução.

* Geral

   * O dimensionamento do lado do navegador pode fazer com que a interface do usuário e as imagens fiquem borradas à medida que o usuário amplia a página. A formatação da interface do usuário também pode ser exibida incorretamente, dependendo do zoom. Isso vai passar para tela cheia.
   * Devido à limitação de tamanho em dispositivos móveis, o Visualizador de mídias mistas usa o gesto de slide para trocar quadros em conjuntos de imagens incorporados, em vez de tocar no componente de amostras incorporado. O componente está lá como um indicador visual.
   * Nos navegadores Internet Explorer e em alguns dispositivos de toque, o modo de tela cheia não ocupa a tela inteira do dispositivo. Em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
   * O botão Fechar não funciona no iOS 8.0 e 8.1, mas não ocorre mais no iOS 8.2

* Galáxia SIII

   * Vazamento de memória observado com visualizadores HTML5 de Zoom e Catálogo eletrônico. A navegação repetida por quadros pode causar falha no navegador.
   * Toque duas vezes no visualizador pode fazer com que a página inteira diminua o zoom em vez de apenas o visualizador com o dimensionamento do lado do navegador ativado.

* Galáxia S4

   * Dispositivo detectado como tablet no modo retrato com Tela cheia marcada nas configurações do navegador.

* Galaxy Nexus

   * Toque duas vezes no visualizador pode fazer com que a página inteira diminua o zoom em vez de apenas o visualizador com o dimensionamento do lado do navegador ativado.

* Galaxy Nexus 10 e Galaxy Comprimido

   * eCatalog mostrando páginas incorretas espalhadas com orientações retrato e paisagem.

* Dispositivos móveis HTC

   * Dispositivos móveis HTC nossos resultados mostram que a incapacidade de desativar o pinch-zoom nativo é um &quot;recurso&quot; do HTC UI wrapper (HTC Sense). Isso pode fazer com que a página inteira amplie o zoom ao usar o gesto de &quot;apertar para zoom&quot; no visualizador. Sugira usar um toque duplo em vez disso.
   * Os ícones do mapa de imagem podem se sobrepor se os mapas de imagem forem pequenos e próximos.

* Vídeo HTML5

   * Internet Explorer 9: imagens de pôster personalizadas não são exibidas.
   * `IntialBitRate` O modificador só é compatível com a reprodução HLS de software e HDS de Flash. Ele não funciona quando a reprodução está usando o reprodutor nativo.
   * A reprodução progressiva de OGG e WebM não é suportada no momento.
   * O dimensionamento do navegador pode fazer com que o reprodutor de vídeo seja exibido com um tamanho incorreto (incluindo as configurações de exibição do painel de controle do sistema operacional do Windows)
   * A busca de vídeo usando o streaming de HLS no Safari pode ser inconsistente.

* Internet Explorer

   * O modo Quirks não é compatível no momento.
   * No momento, o modo de compatibilidade não é compatível.
   * No momento, não há suporte para o Internet Explorer em dispositivos móveis.

* iOS

   * Catálogos eletrônicos grandes podem causar falha no navegador no iPad 2.
   * Os telefones iPhone 6+ são detectados como tablets pelos visualizadores.

* Safari

   * Safari 6.1 ou superior: As configurações de Plug-ins da Internet podem impedir a reprodução de vídeo do Flash.
   * A &quot;busca&quot; de vídeo usando o streaming HLS no Safari pode ser inconsistente.
   * Não é possível buscar o fim do vídeo no Safari 6 usando o streaming HLS.

**Problemas conhecidos e restrições**

* Os modificadores de Exibição de imagem de `iscommands` não são adicionados à solicitação `req=set` por design. Os modificadores que afetam apenas a exibição da imagem funcionam bem. Modificadores que afetam o tamanho devem ser usados em um ativo complexo. Por exemplo,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] O FlyoutIE9 às vezes permanece na tela depois que o mouse é desligado.
* A escala do navegador leva ao redimensionamento incorreto.
* iPad 2: O grande ativo do eCatalog travará o Safari no iOS.
* Todos os visualizadores

   * Marcas d&#39;água, ofuscação e bloqueio não são compatíveis.
   * As predefinições de imagens não são compatíveis.
   * Não há suporte para adicionar ou remover o visualizador do DOM usando `display:none` CSS ou desconectando-o dinamicamente do nó pai no momento.

* Todos os visualizadores HTML5

   * A incorporação do visualizador na tabela pode resultar no dimensionamento incorreto ou no posicionamento do visualizador no modo de tela cheia não nativo. Sugira usar DIVs em vez disso.
   * Os parâmetros com nomes de instância explícitos no código exigem nomes de instância no URL, bem como a substituição (por exemplo, `zoomView.iconfeffect=0`).
   * O recorte de comando do Serviço de Imagens não é compatível no momento.
   * O botão Fechar funciona somente se o visualizador estiver aberto na janela filho.
   * O modificador `iscommands` não suporta modificadores de Exibição de Imagem que afetam o tamanho da imagem.

* Catálogo eletrônico HTML5

   * Navegar para outra página HTML e retornar ocasionalmente faz com que o visualizador seja redefinido para a primeira página.
   * Ocasionalmente, o layout da página é exibido incorretamente após a rotação do dispositivo iOS. O zoom na página corrige o layout.
   * Links internos somente para a página mais à esquerda em spreads de várias páginas. Afeta dispositivos móveis no modo retrato.
   * Links InitalFrame somente para a página mais à esquerda em spreads de várias páginas. Afeta dispositivos móveis no modo retrato.
   * Devido a limitações do navegador, o recurso de impressão não está disponível no IE9.

* Mídia mista HTML5

   * No momento, a reprodução da trilha sonora não é compatível.

* Social HTML5

   * Para renderizar miniaturas corretamente no email de saída, o modificador `serverurl` deve ter um URL absoluto.

* Vídeo HTML5

   * A imagem do pôster pode encontrar o erro &quot;tamanho máximo&quot;. A empresa pode precisar aumentar a configuração de limite para a publicação de fornecimento de imagem.
   * As legendas de vídeo exigem um conjunto de regras da empresa se a hospedagem da página HTML for veiculada a partir de um servidor externo (não de um servidor Scene7). Entre em contato com o Suporte do Adobe para obter assistência.
   * O rastreamento do Analytics pode relatar a porcentagem de reprodução incorreta devido ao buffer
   * O quadro preto em vez da imagem de pôster pode ser exibido em dispositivos iPad ou Android.
   * O quadro preto pode piscar na tela durante o carregamento do visualizador em dispositivos iPad ou Android.
   * As bordas pretas são exibidas no lado do componente VideoPlayer, quando o plano de fundo é definido como branco/transparente em dispositivos iPad.
   * O último quadro do vídeo pode ser distorcido no iPad usando o iOS 7.
   * O macrobloqueio ocasional pode ocorrer durante a busca de vídeo no modo de transmissão HLS em navegadores Chrome, Firefox e Internet Explorer.
      * A imagem de cartaz pode não ser exibida no navegador Microsoft Edge pela primeira vez no visitante.
      * A imagem de cartaz pode se ocultar após o carregamento do vídeo no Internet Explorer 9, quando a reprodução progressiva é usada.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

O Guia do usuário está localizado na pasta Adobe HTML5 Viewer SDK da instalação do cliente. A documentação da API de componente é encontrada na subpasta docs da instalação do cliente.

**Correções de erros para 3.0.2**

* VideoPlayer - Falha ao reproduzir o vídeo no Internet Explorer 11 no Windows 7
* TableOfContents - `initialframe` não afetou o modo retrato em dispositivos móveis para o visualizador de eCatalog HTML5.

**Novos recursos, aprimoramentos e correções de erros do 3.0.1**

* Geral

   * Adição da reprodução de vídeo de streaming HLS como método de entrega de vídeo padrão para a maioria dos sistemas de desktop. O streaming de vídeo HDS baseado em Flash ainda está disponível como uma opção de reprodução alternativa.
   * Adição dos componentes SearchManager, SearchPanel, SearchEffect e SearchButton para suportar o novo recurso de Pesquisa nos visualizadores do eCatalog.
   * Adição de suporte para dispositivos com entrada de mouse e toque em execução no navegador Chrome.
   * Detecção de versão do Android atualizada para oferecer suporte a versões futuras do SO
   * Adicione suporte para orientação da direita para a esquerda em componentes do SDK específicos do Catálogo eletrônico.

* ControlBar

   * Foi adicionada a rolagem opcional para o conteúdo ControlBar caso ele não se encaixe na largura disponível.

* FlyoutzoomView

   * Correção de um problema em que `tip=0,-1,0` causava um erro fora do intervalo.

**Notas de compatibilidade**

* Android 4.x

   * Para desativar o padrão, azul destaque a seguinte regra CSS para ser adicionada ao componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry

   * A reprodução de vídeo pode parar ao alterar fluxos de taxa de bits em conjuntos AVS.

* Cromo

   * Qualquer chamada de API que force a reconstrução de componentes pode ser ignorada devido ao cache interno do Chrome.

* Galáxia SIII

   * Às vezes, o visualizador falha ao carregar em tela cheia.
   * No momento, a Pageview sofre um vazamento de memória no dispositivo.
   * Toque duas vezes no visualizador e na página de zoom de gesto quando a escala do lado do navegador estiver ativa.

* Galaxy Nexus

   * Artefatos exibidos em alguns componentes de exibição.
   * Toque duas vezes no visualizador e na página de zoom de gesto quando a escala do lado do navegador estiver ativa.

* iPad 3

   * O iPad 3 tem uma resolução nativa de 2048x1536. Isso pode causar problemas de exibição se a publicação IS da empresa, o limite de tamanho de imagem definido for menor que isso.

* iPhone4

   * Ícone Reproduzir ícone substituído pelo ícone Reproduzir após a rolagem da página.

* Internet Explorer

   * No IE 10 e modo de tela cheia mais antigo não ocupa a tela inteira, em vez disso, redimensiona o aplicativo para o tamanho da janela do navegador.
   * Não há suporte para o modo de renderização Quirks.
   * No momento, não há suporte para o Internet Explorer em dispositivos móveis.
   * O Util.js pode não ser carregado se estiver incluído de forma assíncrona.
   * O ícone IconEffect bloqueia eventos de clique nos componentes SpinView e ZoomView .

* Reprodutores de vídeo de dispositivo nativo

   * Os componentes da interface de usuário de camadas em relação ao VideoPlayer não são compatíveis quando o VideoPlayer é usado para chamar o player nativo do dispositivo.
   * A reprodução de vídeo no modo nativo é inconsistente no Safari 6.
   * A reprodução nativa substitui o ícone de reprodução pelo ícone de reprodução após a rolagem da página.

* Dispositivos de toque

   * O modo de tela cheia não ocupa a tela inteira do dispositivo, em vez disso, redimensiona o aplicativo para o tamanho da janela do navegador.
   * Cursores personalizados não funcionam em dispositivos de toque.
   * A escala de páginas em dispositivos de toque não é compatível no momento. A incorporação de visualizadores HTML5 requer a meta tag viewport com as configurações apropriadas.

* Xoom

   * Toque duas vezes no visualizador e na página de zoom de gesto quando a escala do lado do navegador estiver ativa.

**Problemas conhecidos e restrições**

* Todos os componentes

   * Nas versões 2.7.2 e anteriores, alguns componentes foram adicionados ao DOM usando a API `insertBefore()` . Como resultado, esses componentes seriam colocados na parte inferior da ordem de empilhamento, independentemente de quando a instância do componente fosse criada em relação a outros componentes. Com a versão 2.8.1, todos os componentes estão usando a API `appendChild()` agora, o que significa que a ordem de empilhamento de componentes corresponderia à ordem de criação da instância.

   * Não há suporte para o uso do modificador `iscommand` para definir o formato do canal alfa da imagem. Em vez disso, use o parâmetro `FMT` do componente.
   * A propriedade de transformação CSS não é suportada no momento.

* Dispositivos de toque

   * O gesto de pinça em dispositivos de toque não gera um evento de zoom

* Contêiner

   * Não há suporte para borda, preenchimento e margens no contêiner. O Adobe sugere adicionar elementos de estilo ao DIV pai.
   * É necessário definir explicitamente o tamanho do contêiner ou os componentes podem ser dimensionados corretamente.

* Componente de impressão

   * Devido a limitações do navegador, no Internet Explorer 9, o componente de impressão pode não dimensionar o conteúdo corretamente no papel.

* Componente IconEffect

   * IconEffect geraria um erro de script no Internet Explorer se `autohide` estivesse desabilitado (definido como `0`).

* Componente ImageMapEffect

   * Atraso com ícone de reposicionamento ao posicionar a imagem no componente de exibição.

* Componente MediaSet

   * Os ativos embutidos solicitam a mesma codificação do URL.

* Componente NavigationView

   * Atualmente, o componente não oferece suporte para redimensionamento.

* Componente PageScrubber

   * No iPhone 5, quando a bolha do PageScrubber é definida como texto, ela exibe artefatos ao deslizar o botão na trilha. Usar `-webkit-background-clip: content;` no estilo funciona em torno do problema.

* Componente SpinView

   * O SpinView às vezes parece congelar após o gesto de deslizamento e girar o dispositivo enquanto a imagem está girando.

* Componente Amostras

   * Ao selecionar uma amostra fora dos limites, 2 destaques são mostrados.
   * Rolagem automática com método `selectSwatch()` funcionando incorretamente.

* VideoPlayer

   * Quadro de vídeo não atualizado se a busca estiver definida como 100% com o fallback definido como automático.
   * O bloqueio ocasional de macro pode ocorrer durante a busca de vídeo no modo de transmissão HLS em navegadores Chrome, Firefox e Internet Explorer.
   * A imagem de cartaz pode não ser exibida no navegador Microsoft Edge pela primeira vez no visitante.
   * A imagem de cartaz pode se ocultar após o carregamento do vídeo no Internet Explorer 9, quando a reprodução progressiva é usada.

## Dynamic Media Image Serving 6.3.2 e Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitário IC - O sinalizador `downsample2x2` não é mais suportado. Esse sinalizador era um analisador de downsampling 2x2 de baixa qualidade que não é mais usado pelo IPS.
* Cabeçalho CORS - Atualmente, o cabeçalho CORS é configurado para solicitações `/is/content/`.

