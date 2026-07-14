---
title: Verificando a instalação
description: Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Verificando a instalação {#verifying-the-installation}

Depois de instalar o Dynamic Media Image Serving, você deve verificar a instalação.

O Servidor de imagens está instalado como um Serviço do Windows.

1. Abra o Painel de Controle de Serviços e verifique se `Dynamic Media Image Serving` está presente com o status `Started`.
1. Abra um navegador da Internet no mesmo host ou em um host diferente e verifique as respostas padrão do servidor:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Verifique a presença de &quot; `imageServer.`&quot; itens na resposta, o que indica que o Servidor de imagens está escutando.

>A verificação adicional pode ser executada usando as páginas de exemplo dos pacotes de Documentação e Demonstração, se instalados.

