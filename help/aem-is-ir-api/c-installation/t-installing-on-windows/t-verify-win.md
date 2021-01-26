---
description: Depois de instalar o Dynamic Media Image Server, verifique a instalação.
seo-description: Depois de instalar o Dynamic Media Image Server, verifique a instalação.
seo-title: Verificação da instalação
solution: Experience Manager
title: Verificação da instalação
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Verificação da instalação{#verifying-the-installation}

Depois de instalar o Dynamic Media Image Server, verifique a instalação.

O Servidor de Imagens está instalado como um Serviço do Windows.

1. Abra o Painel de controle do Campaign Serviços e verifique se &quot;Dynamic Media Image Serving&quot; está presente com o status &quot;Iniciado&quot;.
1. Abra um navegador da Internet no mesmo host ou em outro host e verifique as respostas padrão do servidor:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Verifique a presença de itens &quot; `imageServer.`&quot; na resposta, que indicam que o Servidor de imagens está escutando.
>A verificação adicional pode ser realizada usando as páginas de amostra dos pacotes Documentação e Demonstração, se estiverem instalados.

