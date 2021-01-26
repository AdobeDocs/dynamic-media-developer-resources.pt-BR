---
description: Use este procedimento ao atualizar o Dynamic Media Image Server.
seo-description: Use este procedimento ao atualizar o Dynamic Media Image Server.
seo-title: Atualização do IS 4.7.4 ou posterior
solution: Experience Manager
title: Atualização do IS 4.7.4 ou posterior
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Dynamic Media Image Server.

Se você estiver atualizando de uma versão mais antiga do Serviço de imagem, entre em contato com o suporte para o processo correto.

>[!NOTE]
>
>A pasta [!DNL webapps] pode ser excluída na atualização. Faça backup da pasta [!DNL webapps] antes da atualização.

1. Faça logon no host do servidor com privilégios administrativos.
1. Extraia o conteúdo do arquivo zip de distribuição do Servidor de imagens.
1. Execute setup/setup.exe para iniciar o assistente de instalação.
1. Clique em **[!UICONTROL Next]** para avançar para o Contrato de Licença de Usuário Final (EULA), ler o contrato de licença e clicar em **[!UICONTROL Yes]**.

   A página seguinte exibe as configurações anteriores.
1. Clique em **[!UICONTROL Next]** para start da instalação da atualização.

   >[!NOTE]
   >
   >O instalador faz o backup dos arquivos de configuração do servidor antigos na pasta [!DNL BACKUP/].

1. Quando a instalação estiver concluída, clique em &quot;Concluir&quot; para sair do assistente de instalação.

   Em alguns casos, o assistente de instalação pode solicitar a reinicialização do sistema.

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou quaisquer valores, deve salvar [!DNL server.xml] e reimplementar as alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de colocar o servidor em funcionamento. Consulte a descrição do utilitário `playlog` para obter detalhes.
