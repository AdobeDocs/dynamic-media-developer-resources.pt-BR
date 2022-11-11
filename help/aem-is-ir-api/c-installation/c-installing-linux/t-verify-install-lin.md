---
title: Verificar a instalação
description: Depois de instalar o Image Serving no Linux®, verifique a instalação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verificar a instalação{#verifying-the-installation}

Depois de instalar o Image Serving no Linux®, verifique a instalação.

O Servidor de imagem é instalado como um daemon Linux®.

**Para verificar a instalação**

1. Verifique se a Exibição de imagem está configurada para iniciar automaticamente e se está em execução:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Você deve ter permissões de raiz para executar esses scripts.

1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique as respostas padrão do servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Nas respostas, verifique a presença de itens começando com `imageServer`, que indicam que [!DNL Platform Server] O pôde se comunicar com êxito com o Servidor de imagem.

>A verificação adicional pode ser realizada usando as páginas de exemplo dos pacotes Documentação e Demonstração, se instaladas.
