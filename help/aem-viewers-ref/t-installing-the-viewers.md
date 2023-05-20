---
title: Instalação de vários visualizadores do Dynamic Media no mesmo servidor
description: Instruções para instalar a API do Dynamic Media Viewers.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Instalação de vários visualizadores no mesmo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruções para instalar a API de visualizadores do Dynamic Media.

Instale e teste o Servidor de imagens antes de instalar os visualizadores do Servidor de imagens.

Copie os arquivos dos Visualizadores IS no disco rígido e implante o `s7viewers.war` arquivo na `../ImageServing/webapps` diretório. Consulte a documentação do Servidor de imagens para obter instruções sobre como implantar, iniciar, parar e gerenciar o Servidor de imagens.

>[!NOTE]
>
>Não há instalação de atualização para os visualizadores do Servidor de imagens. A Adobe recomenda que você faça backup de qualquer diretório de visualizadores Dynamic Media (s7views) existente antes de continuar a instalação.

**Para instalar vários visualizadores no mesmo servidor:**

1. Renomeie o visualizador .war para o contexto desejado e implante o arquivo no local desejado.
1. Definir `this.isViewerRoot` parâmetro em `config.js`.
1. Abertura `config.js` na raiz da pasta do visualizador recém-criada.
1. Definir parâmetro `this.isViewerRoot = "/s7viewers"` no contexto da `s7viewers.war` arquivo. Por exemplo, `"/s7viewers-4.0"`.
1. Salve o arquivo e feche-o.
