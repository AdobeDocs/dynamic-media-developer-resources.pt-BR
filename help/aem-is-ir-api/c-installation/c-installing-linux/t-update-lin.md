---
title: Atualização do IS 4.7.4 ou posterior
description: Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux®.

Se estiver atualizando de uma versão mais antiga do Image Serving, entre em contato com o suporte para obter o processo correto.

O [!DNL webapps] pode ser excluída na atualização. Faça backup do [!DNL webapps] pasta antes da atualização.

1. Faça logon no host do servidor com privilégios de raiz.
1. Descompacte e descompacte o arquivo tar de distribuição do Image Serving.
1. No [!DNL setup] pasta, executar [!DNL `./install-is`] para iniciar o assistente de instalação.

   O instalador de atualização verifica a integridade e a versão do pacote instalado. Se o contrato de licença de usuário final (&quot;EULA&quot;) for bem-sucedido, será exibido.
1. Leia o contrato de licença e insira **[!UICONTROL y]** para continuar com a instalação.

   O instalador faz o backup dos arquivos de configuração do servidor antigos no [!DNL BACKUP/] pasta.

   Quando a instalação estiver concluída, a seguinte mensagem será exibida:

   `Image Server was started successfully`

Durante uma atualização, a variável [!DNL ImageServing/conf/server.xml] O arquivo é atualizado para as configurações mais recentes. Se você alterou ou adicionou valores, salve os valores existentes [!DNL server.xml] e reimplemente suas alterações após a atualização.

Após uma instalação de atualização, considere o aquecimento do cache de resposta HTTP antes de colocar o servidor ativo. Consulte a descrição do [!DNL playlog] para obter detalhes.
