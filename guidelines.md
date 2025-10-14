---
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---
# Diretrizes para contribuir com a documentação dos recursos do desenvolvedor do Adobe Dynamic Media

## Filosofia da documentação

O Adobe sabe que os usuários do Adobe Dynamic Media trabalham em ambientes extremamente competitivos, esforçando-se para criar experiências digitais que as destaquem de seus concorrentes. Portanto, é essencial que, ao oferecer novas ferramentas avançadas, o Adobe as complemente com documentação precisa e transparente para permitir que o cliente aproveite imediatamente seu investimento no Dynamic Media e potencialize o ROI.

O objetivo é colocar a documentação atualizada nas mãos dos usuários assim que possível. Portanto, priorizamos uma documentação precisa e utilizável, e nos esforçamos para atualizá-la e aprimorá-la continuamente.

## Contribuições à documentação

Para melhorar continuamente a documentação do, toda a comunidade de usuários do é bem-vinda para contribuir em sua elaboração. Seja por meio de pull requests ou problemas, as melhorias na documentação podem ser correções, esclarecimentos, expansões e exemplos adicionais.

## Padrões de documentação

Embora contribuições à documentação do sejam bem-vindas, sejam em formato de pull requests ou em formato de um problema, elas deverão estar em conformidade com nossos padrões de contribuição e de documentação.

As contribuições que não atenderem a esses padrões poderão ser rejeitadas.

### Nós documentamos casos de uso padrão.

A documentação abrange casos de uso padrão. Casos de uso que não se enquadrarem no escopo de instalação e de uso padrão do produto não farão parte da documentação do.

### Geralmente não documentamos bugs e suas soluções.

A documentação abrange casos de uso padrão. Por essa razão, os bugs, seus efeitos e soluções alternativas não são documentados.

As exceções a essa regra aplicam-se às notas de versão, nas quais problemas conhecidos podem ser listados com possíveis soluções que foram aprovadas pelo Gerenciamento de produtos do.

### As contribuições à documentação não se destinam a responder perguntas técnicas.

Quaisquer ideias para melhorar a documentação do são bem-vindas como contribuições. No entanto, comentários, problemas e pull requests destinam-se a *contribuições* somente. Não são destinadas a responder suas perguntas sobre como usar o Dynamic Media, implementar seu projeto ou resolver problemas técnicos.

Quaisquer dúvidas sobre o uso do Dynamic Media ou erros técnicos devem ser notificados por meio do [Portal de suporte corporativo Experience Cloud](https://experienceleague.adobe.com/pt-br?support-solution=General&support-tab=home#support) ou discutido na [comunidade Experience Manager.](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?profile.language=pt)

***As contribuições à documentação não substituem o Atendimento ao cliente do Adobe*** e quaisquer contribuições que buscam respostas para perguntas relacionadas a suporte são rejeitadas.

### As contribuições devem mencionar claramente as páginas de documentação afetadas.

Se você criar um problema para sugerir melhorias na documentação, deverá incluir links para as páginas afetadas. Se você criar um problema usando a variável **Editar esta página** em uma página de documentação, o problema é criado automaticamente com um link para a página.

Esse processo não se aplica a pull requests, que já fazem referência às páginas afetadas.

## Diretrizes de documentação

Solicitamos que qualquer contribuição à nossa documentação siga determinadas diretrizes de estilo.

Seguir essas diretrizes facilita a análise de sua contribuição, o que agiliza a integração à nossa documentação.

### Idioma e estilo

#### Idioma

* A documentação foi criada e mantida em inglês americano.
* Mantenha as frases o mais simples possível.
* Mantenha a linguagem clara e concisa.

Lembre-se de que os leitores da documentação do estão espalhados ao redor do mundo, e não espera-se que sejam falantes nativos ou fluentes em inglês. Evite linguagem coloquial e mantenha-a o mais clara e simples possível.

#### Siga o Manual de estilo da Microsoft®

[Manual de estilo da Microsoft®](https://learn.microsoft.com/en-us/style-guide/welcome/) O é um guia de estilo disponível gratuitamente. Ele se concentra na documentação de softwares, e a documentação da Dynamic Media o segue sempre que possível.

### Formatação

| Item | Estilo |
|---|---|
| Elemento ou opção da interface do usuário | **negrito** |
| Nome do arquivo, caminho, entrada do usuário, valores de parâmetro | `monospaced` |
| Código, linha de comando | ```Code Block``` |

### Capturas de tela

As capturas de tela devem ser usadas com critério e somente quando uma descrição textual for insuficiente.

Marcadores ou outras anotações em capturas de tela (como quadros vermelhos, setas ou texto) não devem ser usados. O motivo é que as capturas de tela são mais fáceis de reutilizar ou replicar em versões localizadas da documentação.

### Referências específicas à versão

Evite referências diretas a uma versão específica em todo o conteúdo da documentação, sempre que possível. Isso torna a documentação mais flexível e extensível para versões futuras.