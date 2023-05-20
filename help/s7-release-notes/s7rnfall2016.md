---
title: Versão do último trimestre de 2016 da Scene7
description: "As notas de versão mais recentes da versão do último trimestre de 2016 do Adobe Scene7, parte da solução da Adobe Experience Manager no Adobe Experience Cloud."
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Versão do último trimestre de 2016 da Scene7{#scene-fall-release}

Adobe Scene7 As notas de versão mais recentes da parte da solução Adobe Experience Manager no Adobe Experience Cloud do último trimestre de 2016.

## Versão do último trimestre de 2016 da Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

As notas de versão mais recentes do [!DNL Adobe Scene7] Versão do último trimestre de 2016 do [!DNL Adobe Experience Manager] solução no [!DNL Adobe Experience Cloud].

* [Geral](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizadores (Servidor de imagens 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizadores (Servidor de imagens 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizadores (Servidor de imagens 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Visualizador HTML5 SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Serviço de imagem do Dynamic Media Classic 6.3.2 e Renderização de imagem 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Geral {#section-52afeb72ecb34c1585ea67a5051825a2}

A Adobe está animada em anunciar a disponibilidade da entrega de conteúdo HTTP/2 com o benefício geral de um melhor desempenho.

Consulte [Perguntas frequentes sobre entrega de conteúdo HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Sistema de publicação do Scene7 {#section-24487cb493444d808fb7193f0a00cdd4}

Para obter a documentação completa, consulte [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Novos recursos, melhorias e correções de erros**

* Remoção do recurso de recorte de vídeo de [!DNL Adobe Scene7 Publishing System] interface do usuário.
* Autenticação adicionada a todos os servlets do Scene7, quando necessário e possível
* Correção de erros envolvendo a Exibição de lista na lixeira.
* Removido **Criar administrador do Dynamic Media Classic (Scene7)** recurso do usuário do Gerenciamento de usuários devido a preocupações de segurança.
* O FTP WebAdmin agora é compatível com a autenticação OKTA.
* Removido o recurso da senha padrão que foi criada para novos usuários do Portal de mídia.
* Correção de erros envolvendo a senha temporária que foi gerada quando um novo usuário foi adicionado. A senha não atendia aos requisitos de senha necessários.
* Solução de problemas de disco raiz cheio do WebAdmin.
* Correção de erros envolvendo a desativação de um usuário que não é refletida imediatamente na interface do usuário.
* Correção de erros envolvendo a exclusão de um usuário que não permitia recriar o usuário posteriormente.
* Correção de erros envolvendo o email de boas-vindas enviado aos novos usuários do Scene7 que não incluía autenticação para controlar determinadas configurações.
* Correção de erros envolvendo a falha ao recuperar uma lista de pastas FTP se qualquer pasta tivesse caracteres especiais em seu nome.
* Configure provedores de serviços OKTA para ambientes do Scene7.
* Adição de suporte à ID de organização do Experience Cloud para o Viewer Analytics.
* Consumidor SAML do Scene7 implementado.

## Visualizadores (Servidor de imagens 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obter a documentação completa, consulte [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correções de erros do Image Serving 5.5.3**

* Compatibilidade com as bibliotecas RequireJS e DOJO.

   Armazenamento em cache JS consolidado do SDK durante a implantação do visualizador.

## Visualizadores (Servidor de imagens 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obter a documentação completa, consulte [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correções de erros do Image Serving 5.5.2**

* Falha na reprodução do vídeo no Internet Explorer 11 no Windows 7.
* `initialframe` não afetava o modo retrato em dispositivos móveis para o eCatalog HTML5.

## Visualizadores (Servidor de imagens 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obter a documentação completa, consulte [Guia de referência de visualizadores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Novos recursos, melhorias e correções de erros do Servidor de imagens 5.5.1**

* Visualizador de eCatalog do HTML5 com recurso de pesquisa.
* Adição da reprodução de vídeo de transmissão HLS como um método de entrega de vídeo padrão para a maioria dos sistemas de desktop. A transmissão de vídeo HDS baseada em Flash ainda está disponível como uma opção alternativa de reprodução.
* Adicionado suporte para dispositivos com entrada de mouse e toque executando o navegador Chrome.
* Adição do suporte à ID de organização do Experience Cloud na integração do Analytics.
* Atualize a biblioteca JavaScript do AppMeasurement para a versão 1.6.1.
* Adição de suporte para orientação da direita para a esquerda no visualizador do eCatalog.
* Correção de um problema em que `tip=0,-1,0` causou um erro fora do intervalo.

**Notas de compatibilidade**

* BlackBerry®

   * Incompatibilidade com conjuntos AVS mais antigos. Os clientes devem recarregar os conjuntos de AVS para permitir a reprodução.

* Geral

   * O dimensionamento do lado do navegador pode fazer com que a interface do usuário e as imagens fiquem desfocadas à medida que o usuário amplia a página. A formatação da interface também pode ser exibida incorretamente, dependendo do zoom. Esse efeito é transferido para a tela inteira.
   * Devido à limitação de tamanho em dispositivos móveis, o Visualizador de mídia mista usa gestos de deslizamento para trocar quadros em conjuntos de imagens incorporadas, em vez de tocar no componente de amostras incorporadas. O componente está lá como um indicador visual.
   * Em navegadores Internet Explorer e alguns dispositivos de toque, o modo de tela cheia não ocupa a tela inteira do dispositivo. Em vez disso, ele redimensiona o aplicativo para o tamanho da janela do navegador.
   * O botão Fechar não funciona no iOS 8.0 e 8.1, mas não ocorre mais no iOS 8.2

* Galaxy SIII

   * Vazamento de memória observado com visualizadores Zoom e eCatalog HTML5. A navegação repetida pelos quadros pode causar falhas no navegador.
   * O toque duplo no visualizador pode fazer com que a página inteira aplique zoom, em vez de apenas no visualizador com o dimensionamento do lado do navegador ativado.

* Galaxy S4

   * Dispositivo detectado como tablet no modo retrato com Tela cheia nas configurações do navegador.

* Galaxy Nexus

   * O toque duplo no visualizador pode fazer com que a página inteira aplique zoom, em vez de apenas no visualizador com o dimensionamento do lado do navegador ativado.

* Galaxy Nexus 10 e Galaxy Tablet

   * eCatalog mostrando páginas espelhadas incorretas com orientações de retrato e paisagem.

* Dispositivos móveis HTC

   * ADOBE de dispositivos móveis HTC mostram que a incapacidade de desativar o pinch-zoom nativo é um &quot;recurso&quot; do invólucro da interface do usuário HTC (HTC Sense). Esse problema pode fazer com que a página inteira use o zoom ao usar o gesto de &quot;apertar para aplicar zoom&quot; no visualizador. Sugestão: em vez disso, toque duas vezes.
   * Os ícones do mapa de imagem podem se sobrepor se os mapas de imagem forem pequenos e próximos.

* Vídeo HTML5

   * Internet Explorer 9: imagens de pôster personalizadas não são exibidas.
   * `IntialBitRate` O modificador só é compatível com o software HLS e a reprodução de HDS do Flash. Não funciona quando a reprodução está usando o reprodutor nativo.
   * A reprodução progressiva OGG e WebM não é suportada no momento.
   * O dimensionamento do navegador pode fazer com que o reprodutor de vídeo seja exibido em um tamanho incorreto (inclui configurações de exibição do painel de controle do SO Windows).
   * A busca de vídeo usando o streaming HLS no Safari pode ser inconsistente.

* Internet Explorer

   * O modo Quirks não é suportado atualmente.
   * No momento, não há suporte para o modo de compatibilidade.
   * Atualmente, o Internet Explorer em dispositivos móveis não é suportado.

* iOS

   * Catálogos eletrônicos grandes podem causar travamento do navegador no iPad 2.
   * Os telefones iPhone 6+ são detectados como tablets pelos visualizadores.

* Safari

   * Safari 6.1 ou posterior: as configurações de plug-ins da Internet podem impedir a reprodução de vídeo no Flash.
   * A &quot;busca&quot; de vídeo usando a transmissão HLS no Safari pode ser inconsistente.
   * Não é possível buscar o fim do vídeo no Safari 6 usando o streaming HLS.

**Problemas conhecidos e restrições**

* Os modificadores do Servidor de imagens de `iscommands` não são adicionados à `req=set` por design. Os modificadores que afetam apenas a exibição da imagem funcionam bem. Os modificadores que afetam o tamanho devem ser usados em um ativo complexo. Por exemplo,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flyout] O IE9 às vezes permanece na tela após o mouse sair.
* O dimensionamento do navegador leva ao redimensionamento incorreto.
* iPad 2: um grande ativo de eCatalog trava o Safari no iOS.
* Todos os visualizadores

   * Marcas d&#39;água, ofuscação e bloqueio não são suportados.
   * As predefinições de imagem não são compatíveis.
   * Adicionar ou remover o visualizador do DOM usando `display:none` Atualmente, não há suporte para CSS ou para desanexá-lo dinamicamente do nó principal.

* HTML5 Todos os visualizadores

   * A incorporação do visualizador na tabela pode resultar no dimensionamento ou posicionamento incorreto do visualizador no modo de tela cheia não nativo. Sugira usar DIVs.
   * Parâmetros com nomes de instância explícitos no código exigem nomes de instância no URL, além de serem substituídos (por exemplo, `zoomView.iconfeffect=0`).
   * No momento, não há suporte para o recorte do comando do Servidor de imagens.
   * O botão Fechar funciona somente se o visualizador estiver aberto na janela filho.
   * A variável `iscommands` O modificador não oferece suporte a modificadores do Servidor de imagens que afetam o tamanho da imagem.

* eCatalog do HTML5

   * Navegar para outra página de HTML e retornar ocasionalmente faz com que o visualizador redefina para a primeira página.
   * O layout da página ocasionalmente é exibido incorretamente após a rotação do dispositivo iOS. O zoom na página corrige o layout.
   * Links internos somente para a página mais à esquerda em páginas espelhadas múltiplas. Afeta dispositivos móveis no modo retrato.
   * O InitialFrame vincula somente à página mais à esquerda em páginas espelhadas de várias páginas. Afeta dispositivos móveis no modo retrato.
   * Devido às limitações do navegador, o recurso de impressão não está disponível no IE9.

* Mídia mista HTML5

   * A reprodução da trilha sonora não é suportada.

* HTML5 Social

   * Para renderizar miniaturas corretamente em emails de saída, a variável `serverurl` o modificador deve ter um URL absoluto.

* Vídeo HTML5

   * A imagem do pôster pode encontrar o erro de &quot;tamanho máximo&quot;. A empresa deve aumentar a configuração de limite para Publicação no Servidor de imagens.
   * As legendas de vídeo exigem um conjunto de regras de empresa se a hospedagem da página de HTML for fornecida a partir de um servidor externo (não de um servidor Scene7). Entre em contato com o Suporte do Adobe para obter assistência.
   * O rastreamento do Analytics pode relatar porcentagem de reprodução incorreta devido ao buffering
   * A imagem em preto em vez de pôster pode ser exibida em dispositivos iPad ou Android™.
   * O quadro preto pode piscar na tela durante o carregamento do visualizador em dispositivos iPad ou Android™.
   * As bordas pretas são exibidas no lado do componente VideoPlayer quando o plano de fundo é definido como branco/transparente em dispositivos iPad.
   * O último quadro do vídeo pode ser distorcido no iPad usando o iOS 7.
   * O macrobloqueio ocasional pode ocorrer durante a busca de vídeo no modo de streaming HLS em navegadores Chrome, Firefox e Internet Explorer.
      * A imagem do cartaz pode não ser exibida no navegador Microsoft® Edge pela primeira vez.
      * A imagem de cartaz pode se ocultar após o carregamento do vídeo no Internet Explorer 9 quando a reprodução progressiva é usada.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

O Guia do usuário está na pasta Adobe HTML5 Viewer SDK da instalação do cliente. A documentação da API de componentes é encontrada na subpasta docs da instalação do cliente.

**Correções de erros do 3.0.2**

* VideoPlayer - Falha na reprodução do vídeo no Internet Explorer 11 no Windows 7.
* Sumário -  `initialframe` não afetou o modo retrato em dispositivos móveis para o visualizador do eCatalog HTML5.

**Novos recursos, melhorias e correções de erros do 3.0.1**

* Geral

   * Adição da reprodução de vídeo de transmissão HLS como um método de entrega de vídeo padrão para a maioria dos sistemas de desktop. A transmissão de vídeo HDS baseada em Flash ainda está disponível como uma opção alternativa de reprodução.
   * Adição dos componentes SearchManager, SearchPanel, SearchEffect e SearchButton para oferecer suporte ao novo recurso de Pesquisa nos visualizadores do eCatalog.
   * Adição de suporte para dispositivos com entrada de mouse e toque em execução no navegador Chrome.
   * Refatoração da detecção de versão do Android™ para oferecer suporte a versões futuras do sistema operacional.
   * Adicione suporte para orientação da direita para a esquerda em componentes SDK específicos do eCatalog.

* ControlBar

   * Adição da rolagem opcional para o conteúdo ControlBar, caso ele não se encaixe na largura disponível.

* FlyoutzoomView

   * Caso fixo em que `tip=0,-1,0` causou um erro fora do intervalo.

**Notas de compatibilidade**

* Android™ 4.x

   * Para desativar o padrão, realce azul a seguinte regra CSS deve ser adicionada para o componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * A reprodução de vídeo pode ser interrompida ao alterar fluxos de taxa de bits em conjuntos AVS.

* Cromo

   * Quaisquer chamadas de API que forçam a recriação de componentes podem ser ignoradas devido ao armazenamento em cache interno do Chrome.

* Galaxy SIII

   * Às vezes, o visualizador não é carregado na tela cheia.
   * Pageview sofre de um vazamento de memória no dispositivo atualmente.
   * O gesto de toque duplo amplia o visualizador e a página quando o dimensionamento no lado do navegador está ativo.

* Galaxy Nexus

   * Artefatos exibidos em alguns componentes de exibição.
   * O gesto de toque duplo amplia o visualizador e a página quando o dimensionamento no lado do navegador está ativo.

* IPAD 3

   * O iPad 3 tem uma resolução nativa de 2048x1536. Essa resolução pode causar problemas de exibição se o limite de tamanho de imagem da empresa for definido como Publicação IS, inferior.

* iPhone4

   * Ícone de repetição ícone de repetição substituído pelo ícone de reprodução após rolar a página.

* Internet Explorer

   * No IE 10 e modo de tela cheia mais antigo não ocupa a tela inteira, em vez disso, ele apenas redimensiona o aplicativo para o tamanho da janela do navegador.
   * O modo de renderização Quirks não é suportado.
   * Atualmente, o Internet Explorer em dispositivos móveis não é suportado.
   * O Util.js pode falhar ao carregar se incluído de forma assíncrona.
   * O ícone IconEffect bloqueia eventos de clique nos componentes SpinView e ZoomView.

* Players de vídeo de dispositivo nativo

   * Os componentes da interface de camadas no VideoPlayer não são compatíveis quando o VideoPlayer é usado para chamar o reprodutor nativo do dispositivo.
   * A reprodução de vídeo no modo nativo está inconsistente no Safari 6.
   * A reprodução nativa substitui o ícone de repetição pelo ícone de reprodução após rolar a página.

* Dispositivos sensíveis ao toque

   * O modo de tela cheia não ocupa a tela inteira do dispositivo. Em vez disso, ele apenas redimensiona o aplicativo para o tamanho da janela do navegador.
   * Cursores personalizados não funcionam em dispositivos de toque.
   * No momento, não há suporte para o dimensionamento de página em dispositivos de toque. A incorporação de visualizadores HTML5 exige a meta tag viewport com configurações apropriadas.

* Xoom

   * O gesto de toque duplo amplia o visualizador e a página quando o dimensionamento no lado do navegador está ativo.

**Problemas conhecidos e restrições**

* Todos os componentes

   * Nas versões 2.7.2 e anteriores, alguns componentes foram adicionados ao DOM usando `insertBefore()` API. Como resultado, esses componentes se colocavam na parte inferior da ordem de empilhamento, independentemente de quando a instância do componente é criada em relação a outros componentes. Com a versão 2.8.1, todos os componentes estão usando `appendChild()` API agora, o que significa que a ordem de empilhamento dos componentes corresponderia à ordem de criação da instância.

   * Usar `iscommand` não há suporte para o modificador para definir o formato de canal alfa da imagem. Usar componente `FMT` em vez disso.
   * No momento, não há suporte para a propriedade de transformação CSS.

* Dispositivos sensíveis ao toque

   * O gesto de pinçar em dispositivos de toque não gera um evento de zoom

* Container

   * Borda, preenchimento e margens no contêiner não são suportados. Adobe sugere adicionar elementos de estilo ao DIV principal.
   * É necessário definir explicitamente o tamanho do contêiner ou os componentes podem ser dimensionados corretamente.

* Componente de impressão

   * Devido às limitações do navegador, no Internet Explorer 9, o componente de impressão pode não dimensionar o conteúdo corretamente no papel.

* Componente IconEffect

   * O IconEffect gera um erro de script no Internet Explorer se `autohide` está desativado (definido como `0`).

* Componente ImageMapEffect

   * Atraso com o ícone de reposicionamento ao mover a imagem no componente de exibição.

* Componente do MediaSet

   * Os ativos incorporados solicitam a mesma codificação que no URL.

* Componente NavigationView

   * Atualmente, o componente não oferece suporte ao redimensionamento.

* Componente do PageScrubber

   * No iPhone 5, quando a bolha do PageScrubber é definida como texto, ela exibe artefatos ao deslizar o botão ao longo da faixa. Usar `-webkit-background-clip: content;` no estilo, contorna o problema.

* Componente do SpinView

   * Às vezes, o SpinView parece congelar depois de deslizar o dedo e girar o dispositivo enquanto a imagem está girando.

* Componente de amostras

   * Ao selecionar uma amostra fora dos limites, dois realces são mostrados.
   * Rolagem automática com `selectSwatch()` método funcionando incorretamente.

* VideoPlayer

   * O quadro do vídeo não é atualizado se a busca estiver definida como 100%, com o fallback definido como auto.
   * O bloqueio de macro ocasional pode ocorrer durante a busca de vídeo no modo de streaming HLS em navegadores Chrome, Firefox e Internet Explorer.
   * A imagem do cartaz pode não ser exibida no navegador Microsoft® Edge pela primeira vez.
   * A imagem de cartaz pode se ocultar após o carregamento do vídeo no Internet Explorer 9 quando a reprodução progressiva é usada.

## Serviço de imagem do Dynamic Media 6.3.2 e Renderização de imagem 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitário IC - `downsample2x2` O sinalizador não é mais compatível. Esse sinalizador era um downsampler 2x2 de baixa qualidade que não é mais usado pelo IPS.
* Cabeçalho CORS - No momento, o cabeçalho CORS está configurado para `/is/content/` solicitações.
