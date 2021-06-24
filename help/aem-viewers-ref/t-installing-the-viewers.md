---
title: Instalar vários visualizadores do Dynamic Media no mesmo servidor
description: Instruções para instalar a API de visualizadores do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Instalar vários visualizadores no mesmo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruções para instalar a API de visualizadores do Dynamic Media.

Instale e teste o Image Serving antes de instalar os visualizadores do Image Serving.

Copie os arquivos de visualizadores IS no disco rígido e implante o arquivo `s7viewers.war` no diretório `../ImageServing/webapps`. Consulte a documentação do Image Serving para obter instruções sobre como implantar, iniciar, parar e gerenciar o Servidor de imagem.

>[!NOTE]
>
>Não há instalação de atualização para os visualizadores do Image Serving. O Adobe recomenda fazer backup de qualquer diretório existente dos visualizadores Dynamic Media (s7viewers) antes de continuar com a instalação.

**Para instalar vários visualizadores no mesmo servidor:**

1. Renomeie o arquivo .war do visualizador para o contexto desejado e implante o arquivo no local desejado.
1. Defina o parâmetro `this.isViewerRoot` em `config.js`.
1. Abra `config.js` na raiz da pasta de visualizador recém-criada.
1. Defina o parâmetro `this.isViewerRoot = "/s7viewers"` para o contexto do arquivo `s7viewers.war`. Por exemplo, `"/s7viewers-4.0"`.
1. Salve o arquivo e feche-o.
