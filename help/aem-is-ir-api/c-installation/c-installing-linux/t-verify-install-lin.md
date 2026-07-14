---
title: Verificando a instalação
description: Após instalar o Servidor de imagens no Linux®, verifique a instalação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 118
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

