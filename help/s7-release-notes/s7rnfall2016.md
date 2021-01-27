---
description: As notas de versão mais recentes da versão Adobe Scene7 do último trimestre de 2016 fazem parte da solução Adobe Experience Manager no Adobe Marketing Cloud.
solution: Experience Manager
title: Versão do último trimestre de 2016 da Scene7
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '2244'
ht-degree: 0%

---


# Versão do último trimestre de 2016 da Scene7{#scene-fall-release}

As notas de versão mais recentes da versão Adobe Scene7 do último trimestre de 2016 fazem parte da solução Adobe Experience Manager no Adobe Marketing Cloud.

## Versão do último trimestre de 2016 da Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

As notas de versão mais recentes de [!DNL Adobe Scene7] versão do último trimestre de 2016 da solução [!DNL Adobe Experience Manager] no [!DNL Adobe Marketing Cloud].

* [Geral](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizadores (Servidor de imagens 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizadores (Servidor de imagens 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizadores (Servidor de imagens 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Server 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Geral {#section-52afeb72ecb34c1585ea67a5051825a2}

A Adobe está empolgada em anunciar a disponibilidade do delivery HTTP/2 de conteúdo com o benefício geral de um melhor desempenho.

Consulte [Delivery HTTP2 de Perguntas frequentes sobre conteúdo](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Para obter a documentação completa, consulte [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Novos recursos, melhorias e correções de erros**

* Recurso de recuperação de vídeo removido da interface do usuário [!DNL Adobe Scene7 Publishing System].
* Autenticação adicionada a todos os servlets Scene7, quando necessário e possível.
* Correção de erros envolvendo a Visualização da Lista na lata de lixo.
* Remoção do recurso **Criar administrador do Dynamic Media Classic (Scene7)** do usuário do Gerenciamento de usuários devido a problemas de segurança.
* O FTP WebAdmin agora oferece suporte à autenticação OKTA.
* Remoção do recurso da senha padrão que foi criada para novos usuários do Portal de mídia.
* Correção de bug que envolve a senha temporária gerada quando um novo usuário foi adicionado. A senha não atendeu aos requisitos de senha necessários.
* Solução de problemas de disco raiz do WebAdmin cheio.
* A correção de erros que envolve a desativação de um usuário não é refletida imediatamente na interface do usuário.
* Correção de erros que envolve a exclusão de um usuário que não permitiu a recriação do usuário posteriormente.
* Correção de erros envolvendo o email de boas-vindas enviado para novos usuários do Scene7 que não incluíam autenticação para controlar determinadas configurações.
* Correção de erro que envolve a falha ao recuperar uma lista de pasta FTP se qualquer pasta tiver caracteres especiais em seu nome.
* Configure provedores de serviço OKTA para ambientes Scene7.
* Adição de suporte para ID de empresa do Marketing Cloud para o Viewer Analytics.
* Cliente Scene7 SAML implementado.

## Visualizadores (Servidor de imagens 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obter a documentação completa, consulte [Guia de referência do visualizador](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Correções de erros para o Serviço de imagem 5.5.3**

* Compatibilidade com as bibliotecas RequireJS e DOJO.

   Cache JS do SDK consolidado durante a implantação do visualizador.

## Visualizadores (Servidor de imagens 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obter a documentação completa, consulte [Guia de referência do visualizador](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Correções de erros para o Serviço de imagem 5.5.2**

* Falha ao reproduzir o vídeo no Internet Explorer 11 no Windows 7.
* `initialframe` não estava afetando o modo retrato em dispositivos móveis para o eCatalog HTML5.

## Visualizadores (Servidor de imagens 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obter a documentação completa, consulte [Guia de referência do visualizador](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Novos recursos, melhorias e correções de erros para o Serviço de Imagens 5.5.1**

* Visualizador do eCatalog HTML5 com recurso de pesquisa.
* Adicionada a reprodução de vídeo de streaming HLS como um método de delivery de vídeo padrão para a maioria dos sistemas de desktop. O streaming de vídeo HDS baseado em Flashes ainda está disponível como uma opção alternativa de reprodução.
* Adicionado suporte para dispositivos com entrada de mouse e toque que executam o navegador Chrome.
* Adição do suporte à ID de organização do Marketing Cloud à integração do Analytics.
* Atualize a biblioteca JavaScript do AppMeasurement para a versão 1.6.1.
* Adicionado suporte para a orientação da direita para a esquerda no visualizador eCatalog.
* Foi corrigido um problema em que `tip=0,-1,0` causava um erro fora do intervalo.

**Notas de compatibilidade**

* Blackberry

   * Incompatibilidade com conjuntos AVS mais antigos. Os clientes podem precisar fazer upload dos conjuntos AVS novamente para permitir a reprodução.

* Geral

   * O dimensionamento do lado do navegador pode fazer com que a interface do usuário e as imagens fiquem indefinidas à medida que o usuário aumenta o zoom na página. A formatação da interface também pode ser exibida incorretamente dependendo do zoom. Isso será levado para tela cheia.
   * Devido à limitação de tamanho em dispositivos móveis, o Visualizador de mídia mista usa o gesto de slide para trocar quadros em conjuntos de imagens incorporados, em vez de tocar no componente de amostras incorporado. O componente está lá como um indicador visual.
   * Nos navegadores Internet Explorer e em alguns dispositivos de toque, o modo de tela cheia não ocupa a tela inteira do dispositivo. Em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
   * O botão Fechar não funciona no iOS 8.0 e 8.1, mas não ocorre mais no iOS 8.2

* Galaxy SIII

   * Vazamento de memória observado com visualizadores HTML5 de Zoom e eCatalog. A navegação repetida pelos quadros pode fazer com que o navegador falhe.
   * O toque de duplo no visualizador pode fazer com que a página inteira aumente o zoom em vez de apenas o visualizador com a escala ativada no navegador.

* Galaxy S4

   * Dispositivo detectado como tablet no modo retrato com tela cheia marcada nas configurações do navegador.

* Galaxy Nexus

   * O toque de duplo no visualizador pode fazer com que a página inteira aumente o zoom em vez de apenas o visualizador com a escala ativada no navegador.

* Galaxy Nexus 10 e Galaxy

   * eCatálogo mostrando páginas espelhadas incorretas com orientações retrato e paisagem.

* Dispositivos móveis HTC

   * Dispositivos móveis HTC nossos achados mostram que a incapacidade de desativar o zoom nativo de aproximação é um &quot;recurso&quot; do invólucro HTC UI (HTC Sense). Isso pode fazer com que a página inteira aumente o zoom ao usar o gesto de &quot;juntar zoom&quot; no visualizador. Sugira usar duplo-toque em vez disso.
   * Os ícones do mapa de imagem podem se sobrepor se os mapas de imagem forem pequenos e próximos.

* Vídeo HTML5

   * Internet Explorer 9: as imagens de pôster personalizadas não são exibidas.
   * `IntialBitRate` só há suporte para modificador com HLS de software e reprodução HDS de Flash. Ela não funciona quando a reprodução está usando o player nativo.
   * A reprodução progressiva OGG e WebM não é suportada neste momento.
   * A escala do navegador pode fazer com que o player de vídeo seja exibido em um tamanho incorreto (incluindo as configurações de exibição do painel de controle do SO do Windows)
   * A busca de vídeo usando streaming HLS no Safari pode ser inconsistente.

* Internet Explorer

   * O modo Quirks não é compatível no momento.
   * O modo de compatibilidade não é suportado no momento.
   * O Internet Explorer em dispositivos móveis não é suportado no momento.

* iOS

   * Catálogos grandes podem causar falhas no navegador no iPad 2.
   * Os telefones iPhone 6+ são detectados como tablets pelos visualizadores.

* Safari

   * Safari 6.1 ou posterior: As configurações de plug-ins da Internet podem impedir a reprodução do vídeo do Flash.
   * A &quot;busca&quot; de vídeo usando o streaming de HLS no Safari pode ser inconsistente.
   * Não é possível buscar o fim do vídeo no Safari 6 usando o streaming HLS.

**Problemas conhecidos e restrições**

* Os modificadores do Servidor de imagens de `iscommands` não são adicionados à solicitação `req=set` por padrão. Os modificadores que afetam apenas a exibição da imagem funcionam bem. Modificadores que afetam o tamanho devem ser usados em um ativo complexo. Por exemplo,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [O ] FlyoutIE9 às vezes permanece na tela após o mouse desligar.
* A escala do navegador leva ao redimensionamento incorreto.
* iPad 2: O grande ativo do eCatalog travará o Safari no iOS.
* Todos os visualizadores

   * Marcas d&#39;água, ofuscação e bloqueio não são suportadas.
   * As predefinições de imagens não são suportadas.
   * No momento, não há suporte para adicionar ou remover o visualizador do DOM usando `display:none` CSS ou desconectando-o dinamicamente do nó pai.

* Todos os visualizadores HTML5

   * A incorporação do visualizador na tabela pode resultar em dimensionamento ou posicionamento incorreto do visualizador no modo de tela cheia não nativo. Sugira usar DIVs em vez disso.
   * Parâmetros com nomes de instâncias explícitos no código exigem nomes de instâncias no URL, além de serem substituídos (por exemplo, `zoomView.iconfeffect=0`).
   * O recorte de comando do Servidor de Imagens não é suportado no momento.
   * O botão Fechar funciona somente se o visualizador estiver aberto na janela secundária.
   * O modificador `iscommands` não suporta modificadores do Servidor de imagens que afetam o tamanho da imagem.

* eCatalog HTML5

   * Navegar para outra página HTML e retornar ocasionalmente faz com que o visualizador redefina para a primeira página.
   * Ocasionalmente, o layout da página é exibido incorretamente após a rotação do dispositivo iOS. O zoom na página corrige o layout.
   * Links internos somente para a página mais à esquerda em páginas espelhadas múltiplas. Afeta dispositivos móveis no modo retrato.
   * O InitalFrame vincula somente à página mais à esquerda em páginas espelhadas múltiplas. Afeta dispositivos móveis no modo retrato.
   * Devido a limitações do navegador, o recurso de impressão não está disponível no IE9.

* Mídia mista HTML5

   * A reprodução da trilha sonora não é suportada no momento.

* HTML5 Social

   * Para renderizar miniaturas corretamente no email de saída, o modificador `serverurl` deve ter um URL absoluto.

* Vídeo HTML5

   * A imagem do pôster pode encontrar o erro &quot;tamanho máximo&quot;. A empresa pode precisar aumentar a configuração de limite para o Image Serving Publish.
   * As legendas de vídeo exigem um conjunto de regras de empresa se a hospedagem da página HTML for fornecida por um servidor externo (não por um servidor Scene7). Entre em contato com o Suporte ao Adobe para obter assistência.
   * O rastreamento do Analytics pode relatar uma porcentagem de reprodução incorreta devido ao buffering
   * O quadro preto em vez da imagem de pôster pode ser exibido em dispositivos iPad ou Android.
   * O quadro preto pode piscar na tela durante o carregamento do visualizador em dispositivos iPad ou Android.
   * Bordas pretas são exibidas ao lado do componente VideoPlayer quando o plano de fundo é definido para branco/transparente em dispositivos iPad.
   * O último quadro do vídeo pode estar distorcido no iPad usando o iOS 7.
   * O macrobloqueio ocasional pode ocorrer durante a busca de vídeo no modo de streaming HLS nos navegadores Chrome, Firefox e Internet Explorer.
      * A imagem de cartaz pode não ser exibida no navegador Microsoft Edge pela primeira vez no visitante.
      * A imagem de pôster pode ser ocultada após o carregamento do vídeo no Internet Explorer 9 quando a reprodução progressiva for usada.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

O Guia do usuário está localizado na pasta Adobe HTML5 Viewer SDK da instalação do cliente. A documentação da API do componente é encontrada na subpasta docs da instalação do cliente.

**Correções de erros para 3.0.2**

* VideoPlayer - Falha na reprodução do vídeo no Internet Explorer 11 no Windows 7
* TableOfContents - `initialframe` não afetou o modo retrato em dispositivos móveis para o visualizador eCatalog HTML5.

**Novos recursos, melhorias e correções de erros do 3.0.1**

* Geral

   * Adicionada a reprodução de vídeo de streaming HLS como um método de delivery de vídeo padrão para a maioria dos sistemas de desktop. O streaming de vídeo HDS baseado em Flashes ainda está disponível como uma opção alternativa de reprodução.
   * Adicionados os componentes SearchManager, SearchPanel, SearchEffect e SearchButton para suportar o novo recurso de Pesquisa nos visualizadores eCatalog.
   * Adicionado suporte para dispositivos com entrada de mouse e toque em execução no navegador Chrome.
   * Detecção de versão do Android atualizada para suportar versões futuras do SO
   * Adicione suporte para a orientação da direita para a esquerda em componentes SDK específicos do eCatalog.

* ControlBar

   * Adição da rolagem opcional para o conteúdo da ControlBar caso ele não se ajuste à largura disponível.

* FlyoutzoomView

   * Corrigido o caso em que `tip=0,-1,0` causava um erro fora do intervalo.

**Notas de compatibilidade**

* Android 4.x

   * Para desativar o padrão, realce azul a seguinte regra CSS precisa ser adicionada para o componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * A reprodução de vídeo pode parar ao alterar fluxos de taxa de bits em conjuntos AVS.

* Cromo

   * Qualquer chamada de API que force a reconstrução de componentes pode ser ignorada devido ao cache interno do Chrome.

* Galaxy SIII

   * Às vezes, o visualizador falha ao carregar em tela cheia.
   * No momento, o Pageview sofre de um vazamento de memória no dispositivo.
   * O gesto de toque no duplo amplia o visualizador e a página quando a escala no navegador está ativa.

* Galaxy Nexus

   * Artefatos exibidos sobre alguns componentes de visualização.
   * O gesto de toque no duplo amplia o visualizador e a página quando a escala no navegador está ativa.

* iPad 3

   * O iPad 3 tem uma resolução nativa de 2048 x 1536. Isso pode causar problemas de exibição se a empresa for publicada, o limite de tamanho da imagem definido for menor que esse limite.

* iPhone4

   * Ícone Reproduzir com efeito de ícone substituído pelo ícone Reproduzir após a página de rolagem.

* Internet Explorer

   * No IE 10 e modo de tela cheia mais antigo não ocupa tela inteira, em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
   * O modo de renderização Quirks não é suportado.
   * O Internet Explorer em dispositivos móveis não é suportado no momento.
   * O Util.js pode falhar ao carregar se incluído de forma assíncrona.
   * O ícone IconEffect bloqueia eventos de clique nos componentes SpinView e ZoomView.

* players de vídeo de dispositivo nativo

   * Os componentes da interface de layout em VideoPlayer não são suportados quando o VideoPlayer é usado para chamar o player nativo do dispositivo.
   * A reprodução de vídeo no modo nativo é inconsistente no Safari 6.
   * A reprodução nativa substitui o ícone de reprodução pelo ícone de reprodução após a página de rolagem.

* Dispositivos de toque

   * O modo de tela cheia não ocupa a tela inteira do dispositivo, em vez disso, ele apenas redimensiona o aplicativo para o tamanho da janela do navegador.
   * Cursores personalizados não funcionam em dispositivos de toque.
   * A escala de páginas em dispositivos de toque não é suportada no momento. A incorporação de visualizadores HTML5 requer a tag meta viewport com as configurações apropriadas.

* Xoom

   * O gesto de toque no duplo amplia o visualizador e a página quando a escala no navegador está ativa.

**Problemas conhecidos e restrições**

* Todos os componentes

   * Nas versões 2.7.2 e anteriores, alguns componentes foram adicionados ao DOM usando a API `insertBefore()`. Como resultado, esses componentes seriam colocados na parte inferior da ordem de empilhamento, independentemente de quando a instância do componente fosse criada em relação a outros componentes. Com a versão 2.8.1, todos os componentes estão usando a API `appendChild()` agora, o que significa que a ordem de empilhamento de componentes corresponderia à ordem de criação da instância.

   * Não há suporte para o uso do modificador `iscommand` para definir o formato de canal alfa da imagem. Em vez disso, use o parâmetro `FMT` do componente.
   * A propriedade de transformação CSS não é suportada no momento.

* Dispositivos de toque

   * O gesto de aperto em dispositivos de toque não gera um evento de zoom

* Container

   * Borda, preenchimento e margens no container não são suportados. O Adobe sugere adicionar elementos de estilo ao DIV pai.
   * É necessário definir explicitamente o tamanho do container ou os componentes podem ser dimensionados corretamente.

* Componente de impressão

   * Devido a limitações do navegador, no Internet Explorer 9, o componente de impressão pode não dimensionar o conteúdo corretamente no papel.

* Componente IconEffect

   * IconEffect gera um erro de script no Internet Explorer se `autohide` estiver desativado (definido como `0`).

* Componente ImageMapEffect

   * Atraso com ícone de reposicionamento ao deslocar a imagem no componente de visualização.

* Componente MediaSet

   * Os ativos incorporados solicitam a mesma codificação que no URL.

* Componente NavigationView

   * Atualmente, o componente não oferece suporte para redimensionamento.

* Componente PageScrubber

   * No iPhone 5, quando a bolha do PageScrubber está definida como texto, ela exibe artefatos ao deslizar o botão ao longo da faixa. Usar `-webkit-background-clip: content;` no estilo funciona em torno do problema.

* Componente SpinView

   * Às vezes, o SpinView parece congelar após o gesto de deslizar e girar o dispositivo enquanto a imagem está girando.

* Componente de amostras

   * Ao selecionar uma amostra fora dos limites, 2 realces são mostrados.
   * A rolagem automática com o método `selectSwatch()` está funcionando incorretamente.

* VideoPlayer

   * Quadro de vídeo não atualizado se a busca estiver definida como 100% com o fallback definido como auto.
   * O bloqueio ocasional de macro pode ocorrer durante a busca de vídeo no modo de streaming HLS nos navegadores Chrome, Firefox e Internet Explorer.
   * A imagem de cartaz pode não ser exibida no navegador Microsoft Edge pela primeira vez no visitante.
   * A imagem de pôster pode ser ocultada após o carregamento do vídeo no Internet Explorer 9 quando a reprodução progressiva for usada.

## Dynamic Media Image Serving 6.3.2 e Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitário IC - o sinalizador `downsample2x2` não é mais suportado. Esse sinalizador era um redutor de qualidade 2x2 ruim que não é mais usado pelo IPS.
* Cabeçalho CORS - Atualmente, o cabeçalho CORS está configurado para `/is/content/` solicitações.

