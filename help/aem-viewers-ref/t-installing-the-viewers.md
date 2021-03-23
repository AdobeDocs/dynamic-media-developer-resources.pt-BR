---
title: Instalar vários visualizadores do Dynamic Media no mesmo servidor
description: Instruções para instalar a API de visualizadores do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Instalar vários visualizadores no mesmo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruções para instalar a API de visualizadores do Dynamic Media.

Instale e teste o Image Serving antes de instalar os visualizadores do Image Serving.

Copie os arquivos de visualizadores IS no disco rígido e implante o arquivo `s7viewers.war` no diretório `../ImageServing/webapps`. Consulte a documentação do Image Serving para obter instruções sobre como implantar, iniciar, parar e gerenciar o Servidor de imagem.

>[!NOTE]
>
>Não há instalação de atualização para os visualizadores do Image Serving. O Adobe recomenda fazer backup de qualquer diretório existente dos visualizadores Dynamic Media (s7viewers) antes de continuar com a instalação.

**Para instalar vários visualizadores no mesmo servidor**

1. Renomeie o arquivo .war do visualizador para o contexto desejado e implante o arquivo no local desejado.
1. Defina o parâmetro `this.isViewerRoot` em `config.js`.
1. Abra `config.js` localizado na raiz da pasta de visualizador recém-criada.
1. Defina o parâmetro `this.isViewerRoot = "/s7viewers"` para o contexto do arquivo `s7viewers.war`. Por exemplo, `"/s7viewers-4.0"`.
1. Salve o arquivo e feche-o.
