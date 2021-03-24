---
description: Use esse procedimento ao atualizar o Dynamic Media Image Serving.
solution: Experience Manager
title: Atualização do IS 4.7.4 ou posterior
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use esse procedimento ao atualizar o Dynamic Media Image Serving.

Se estiver atualizando de uma versão mais antiga do Image Serving, entre em contato com o suporte para obter o processo correto.

>[!NOTE]
>
>A pasta [!DNL webapps] pode ser excluída na atualização. Faça o backup da pasta [!DNL webapps] antes da atualização.

1. Faça logon no host do servidor com privilégios administrativos.
1. Extraia o conteúdo do arquivo zip de distribuição do Serviço de Imagens.
1. Execute setup/setup.exe para iniciar o assistente de instalação.
1. Clique em **[!UICONTROL Next]** para avançar para o Contrato de Licença de Usuário Final (EULA), leia o contrato de licença e clique em **[!UICONTROL Yes]**.

   A próxima página exibe as configurações anteriores.
1. Clique em **[!UICONTROL Next]** para iniciar a instalação da atualização.

   >[!NOTE]
   >
   >O instalador faz o backup dos arquivos de configuração do servidor antigos na pasta [!DNL BACKUP/].

1. Quando a instalação estiver concluída, clique em &quot;Concluir&quot; para sair do assistente de instalação.

   Em alguns casos, o assistente de instalação pode solicitar a reinicialização do sistema.

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou algum valor, deve salvar seu [!DNL server.xml] existente e reimplementar as alterações após a atualização.

Após uma instalação de atualização, considere o aquecimento do cache de resposta HTTP antes de colocar o servidor em funcionamento. Consulte a descrição do utilitário `playlog` para obter detalhes.
