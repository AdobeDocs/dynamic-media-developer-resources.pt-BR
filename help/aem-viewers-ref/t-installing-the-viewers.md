---
description: Instruções para instalar a API do visualizador de mídia dinâmica.
seo-description: Instruções para instalar a API do visualizador de mídia dinâmica.
seo-title: Instalação de vários visualizadores no mesmo servidor
solution: Experience Manager
title: Instalação de vários visualizadores no mesmo servidor
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Instalação de vários visualizadores no mesmo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruções para instalar a API de visualizadores do Dynamic Media.

Instale e teste o Serviço de imagem antes de instalar os visualizadores do Servidor de imagens.

Copie os arquivos IS Viewers para o disco rígido e implante o `s7viewers.war` arquivo no `../ImageServing/webapps` diretório. Consulte a documentação do Servidor de imagens para obter instruções sobre como implantar, start, parar e gerenciar o Servidor de imagens.

>[!NOTE]
>
>Não há instalação de atualização para os visualizadores do Servidor de imagens. A Adobe recomenda que você faça backup de qualquer diretório de visualizadores do Dynamic Media existente antes de continuar com a instalação.

**Para instalar os visualizadores no mesmo servidor**

1. Renomeie o visualizador .war para o contexto desejado e implante o arquivo no local desejado.
1. Defina o `this.isViewerRoot` parâmetro em `config.js`.
1. Abra `config.js` localizado na raiz da pasta do visualizador recém-criada.
1. Defina o parâmetro `this.isViewerRoot = "/s7viewers"` para o contexto do `s7viewers.war` arquivo. Por exemplo, `"/s7viewers-4.0"`. Salve e feche o arquivo.
1. Salve o arquivo e feche-o.
