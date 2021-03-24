---
description: Depois de instalar o Image Serving no Linux, verifique a instalação.
solution: Experience Manager
title: Verificar a instalação
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Verificando a instalação{#verifying-the-installation}

Depois de instalar o Image Serving no Linux, verifique a instalação.

O Servidor de imagem é instalado como um daemon Linux.

**Para verificar a instalação**

1. Verifique se a Exibição de imagem está configurada para iniciar automaticamente e se está em execução:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Você deve ter permissões de raiz para executar esses scripts.

1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique a(s) resposta(s) padrão(s) do servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Nas respostas, verifique a presença de itens começando com &quot; `imageServer.`&quot;, que indicam que o Servidor de Plataforma conseguiu se comunicar com êxito com o Servidor de Imagens.
>A verificação adicional pode ser realizada usando as páginas de exemplo dos pacotes Documentação e Demonstração, se instaladas.

