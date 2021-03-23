---
description: Depois de instalar o Image Serving no Linux, verifique a instalação.
seo-description: Depois de instalar o Image Serving no Linux, verifique a instalação.
seo-title: Verificar a instalação
solution: Experience Manager
title: Verificar a instalação
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
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

