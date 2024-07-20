---
title: Verificando a instalação
description: Após instalar o Servidor de imagens no Linux®, verifique a instalação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verificando a instalação{#verifying-the-installation}

Após instalar o Servidor de imagens no Linux®, verifique a instalação.

O Servidor de imagens é instalado como um daemon Linux®.

**Para verificar a instalação**

1. Verifique se o Servidor de imagens está configurado para iniciar automaticamente e se está em execução:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Você deve ter permissões raiz para executar esses scripts.

1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique as respostas padrão do servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Nas respostas, verifique a presença de itens começando com `imageServer`, o que indica que o [!DNL Platform Server] pode se comunicar com o Servidor de imagens com êxito.

>A verificação adicional pode ser executada usando as páginas de exemplo dos pacotes de Documentação e Demonstração, se instalados.
