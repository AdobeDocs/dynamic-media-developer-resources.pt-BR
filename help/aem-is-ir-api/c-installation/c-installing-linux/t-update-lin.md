---
title: Atualizando do IS 4.7.4 ou posterior
description: Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
TQID: 'https://experienceleague.adobe.com/RGRlIuemg6bPstlymZg7Ajr9i2ANq-HNjoIULaJydfs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 0%

---

# Atualizando do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux®.

Se você estiver atualizando de uma versão mais antiga do Servidor de imagens, entre em contato com o suporte para obter o processo correto.

A pasta [!DNL webapps] pode ser excluída na atualização. Faça backup da pasta [!DNL webapps] antes de atualizar.

1. Faça logon no host do servidor com privilégios de raiz.
1. Descompacte e descompacte o arquivo tar de distribuição do Servidor de imagens.
1. Na pasta [!DNL setup], execute [!DNL `./install-is`] para iniciar o assistente de instalação.

   O instalador da atualização verifica a integridade e a versão do pacote instalado. Se for bem-sucedido, o Contrato de licença de usuário final (&quot;EULA&quot;) será exibido.
1. Leia o contrato de licença e digite **[!UICONTROL y]** para prosseguir com a instalação.

   O instalador faz backup dos arquivos de configuração do servidor antigo na pasta [!DNL BACKUP/].

   Quando a instalação estiver concluída, a seguinte mensagem será exibida:

   `Image Server was started successfully`

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou valores, salve o [!DNL server.xml] existente e reimplemente as alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de ativar o servidor. Consulte a descrição do utilitário [!DNL playlog] para obter detalhes.

