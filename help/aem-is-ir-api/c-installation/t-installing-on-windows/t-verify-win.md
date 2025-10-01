---
title: Verificando a instalação
description: Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Verificando a instalação {#verifying-the-installation}

Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.

O Servidor de imagens está instalado como um Serviço do Windows.

1. Abra o Painel de Controle de Serviços e verifique se `Dynamic Media Image Serving` está presente com o status `Started`.
1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique as respostas padrão do servidor:

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Verifique a presença de &quot; `imageServer.`&quot; itens na resposta, o que indica que o Servidor de imagens está escutando.

>A verificação adicional pode ser executada usando as páginas de exemplo dos pacotes de Documentação e Demonstração, se instalados.
