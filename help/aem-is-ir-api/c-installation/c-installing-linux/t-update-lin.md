---
description: Use esse procedimento ao atualizar o Dynamic Media Image Serving no Linux.
solution: Experience Manager
title: Atualização do IS 4.7.4 ou posterior
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use esse procedimento ao atualizar o Dynamic Media Image Serving no Linux.

Se estiver atualizando de uma versão mais antiga do Image Serving, entre em contato com o suporte para obter o processo correto.

A pasta [!DNL webapps] pode ser excluída na atualização. Faça backup da pasta [!DNL webapps] antes de atualizar.

1. Faça logon no host do servidor com privilégios de raiz.
1. Descompacte e descompacte o arquivo tar de distribuição do Image Serving.
1. Execute [!DNL ./install-is] para iniciar o assistente de instalação localizado na pasta [!DNL setup].

   O instalador de atualização verifica a integridade e a versão do pacote instalado. Se o contrato de licença de usuário final (&quot;EULA&quot;) for bem-sucedido, será exibido.
1. Leia o contrato de licença e digite &quot;**[!UICONTROL y]**&quot; para prosseguir com a instalação.

   O instalador faz o backup dos arquivos de configuração do servidor antigos na pasta [!DNL BACKUP/].

   Quando a instalação estiver concluída, a seguinte mensagem será mostrada:

   `Image Server was started successfully`

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou algum valor, deve salvar seu [!DNL server.xml] existente e reimplementar as alterações após a atualização.

Após uma instalação de atualização, considere o aquecimento do cache de resposta HTTP antes de colocar o servidor em funcionamento. Consulte a descrição do utilitário [!DNL playlog] para obter detalhes.
