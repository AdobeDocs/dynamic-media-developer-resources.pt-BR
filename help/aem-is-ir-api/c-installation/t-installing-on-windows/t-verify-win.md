---
description: Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.
solution: Experience Manager
title: Verificar a instalação
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verificar a instalação{#verifying-the-installation}

Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.

O Servidor de Imagens é instalado como um Serviço do Windows.

1. Abra o Painel de controle dos serviços e verifique se &quot;Dynamic Media Image Serving&quot; está presente com o status &quot;Started&quot; (Iniciado).
1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique as respostas padrão do servidor:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Verifique a presença de &quot; `imageServer.`&quot; itens na resposta, que indicam que o Servidor de Imagem está escutando.
>A verificação adicional pode ser realizada usando as páginas de exemplo dos pacotes Documentação e Demonstração, se instaladas.
