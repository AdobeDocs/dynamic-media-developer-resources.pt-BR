---
title: Instalação de vários visualizadores Dynamic Media no mesmo servidor
description: Instruções para instalar a API do Dynamic Media Viewers.
solution: Experience Manager
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Instalação de vários visualizadores no mesmo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruções para instalar a API de visualizadores do Dynamic Media.

Instale e teste o Serviço de imagem antes de instalar os visualizadores do Servidor de imagens.

Copie os arquivos IS Viewers para o disco rígido e implante o arquivo `s7viewers.war` no diretório `../ImageServing/webapps`. Consulte a documentação do Servidor de imagens para obter instruções sobre como implantar, start, parar e gerenciar o Servidor de imagens.

>[!NOTE]
>
>Não há instalação de atualização para os visualizadores do Servidor de imagens. O Adobe recomenda que você faça backup de qualquer diretório existente do visualizador do Dynamic Media (s7viewers) antes de continuar com a instalação.

**Para instalar vários visualizadores no mesmo servidor**

1. Renomeie o visualizador .war para o contexto desejado e implante o arquivo no local desejado.
1. Defina o parâmetro `this.isViewerRoot` em `config.js`.
1. Abra `config.js`, localizado na raiz da pasta do visualizador recém-criada.
1. Defina o parâmetro `this.isViewerRoot = "/s7viewers"` para o contexto do arquivo `s7viewers.war`. Por exemplo, `"/s7viewers-4.0"`.
1. Salve o arquivo e feche-o.
