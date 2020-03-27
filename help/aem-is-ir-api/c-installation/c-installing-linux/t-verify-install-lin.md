---
description: Depois de instalar o Image Serving no Linux, verifique a instalação.
seo-description: Depois de instalar o Image Serving no Linux, verifique a instalação.
seo-title: Verificação da instalação
solution: Experience Manager
title: Verificação da instalação
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verificação da instalação{#verifying-the-installation}

Depois de instalar o Image Serving no Linux, verifique a instalação.

O Servidor de imagens está instalado como um daemon Linux.

**Para verificar a instalação**

1. Verifique se o Servidor de imagens está configurado para start automaticamente e se está em execução:

   `> /sbin/service ImageServing status`

   >[!NOTE] {class=&quot;- tópico/observação &quot;}
   >
   >É necessário ter permissões de raiz para executar esses scripts.

1. Abra um navegador da Internet no mesmo host ou em outro host e verifique as respostas padrão do servidor:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Nas respostas, verifique a presença de itens que começam com &quot; `imageServer.`&quot;, o que indica que o Servidor de plataforma conseguiu se comunicar com êxito com o Servidor de imagens.
>A verificação adicional pode ser realizada usando as páginas de amostra dos pacotes Documentação e Demonstração, se estiverem instalados.

