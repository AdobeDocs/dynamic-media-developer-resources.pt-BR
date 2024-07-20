---
title: Iniciando ou interrompendo no Linux®
description: Há duas opções para iniciar ou parar o Servidor de imagens no Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Iniciando ou interrompendo no Linux® {#starting-or-stopping-on-linux}

Há duas opções para iniciar ou parar o Servidor de imagens no Linux®.

* O script para verificar o status do Servidor de Imagens, ou para iniciar e parar o Servidor de Imagens, é encontrado na pasta [!DNL ImageServing/bin]:

  `ImageServing.sh {start|stop|restart|status}`
* A alternativa a seguir deve ser familiar aos administradores do sistema:

  `/sbin/service ImageServing {start|stop|status}`
