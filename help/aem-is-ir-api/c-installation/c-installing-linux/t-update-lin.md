---
title: Atualizando do IS 4.7.4 ou posterior
description: Use este procedimento ao atualizar o Servidor de imagens da Dynamic Media no Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Atualizando do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Servidor de imagens da Dynamic Media no Linux®.

Se você estiver atualizando de uma versão mais antiga do Servidor de imagens, entre em contato com o suporte para obter o processo correto.

A variável [!DNL webapps] a pasta pode ser excluída na atualização. Faça backup do [!DNL webapps] pasta antes da atualização.

1. Faça logon no host do servidor com privilégios de raiz.
1. Descompacte e descompacte o arquivo tar de distribuição do Servidor de imagens.
1. No [!DNL setup] pasta, execute [!DNL `./install-is`] para iniciar o assistente de instalação.

   O instalador da atualização verifica a integridade e a versão do pacote instalado. Se for bem-sucedido, o Contrato de licença de usuário final (&quot;EULA&quot;) será exibido.
1. Leia o contrato de licença e insira **[!UICONTROL y]** para prosseguir com a instalação.

   O instalador faz o backup dos arquivos antigos de configuração do servidor no [!DNL BACKUP/] pasta.

   Quando a instalação estiver concluída, a seguinte mensagem será exibida:

   `Image Server was started successfully`

Durante uma atualização, a variável [!DNL ImageServing/conf/server.xml] O arquivo foi atualizado para as configurações mais recentes. Se você tiver alterado ou adicionado algum valor, salve o existente [!DNL server.xml] e reimplemente suas alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de ativar o servidor. Consulte a descrição do [!DNL playlog] para obter detalhes.
