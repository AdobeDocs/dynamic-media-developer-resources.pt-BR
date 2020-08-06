---
description: Use este procedimento ao atualizar o Scene7 Image Server.
seo-description: Use este procedimento ao atualizar o Scene7 Image Server.
seo-title: Atualização do IS 4.7.4 ou posterior
solution: Experience Manager
title: Atualização do IS 4.7.4 ou posterior
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Scene7 Image Server.

Se você estiver atualizando de uma versão mais antiga do Serviço de imagem, entre em contato com o suporte para o processo correto.

>[!NOTE]
>
>A [!DNL webapps] pasta pode ser excluída na atualização. Faça backup da [!DNL webapps] pasta antes da atualização.

1. Faça logon no host do servidor com privilégios administrativos.
1. Extraia o conteúdo do arquivo zip de distribuição do Servidor de imagens.
1. Execute setup/setup.exe para iniciar o assistente de instalação.
1. Clique para avançar **[!UICONTROL Next]** para o Contrato de Licença de Usuário Final (EULA), ler o contrato de licença e clicar em **[!UICONTROL Yes]**.

   A página seguinte exibe as configurações anteriores.
1. Clique em **[!UICONTROL Next]** para start da instalação de atualização.

   >[!NOTE]
   >
   >O instalador faz o backup dos arquivos de configuração do servidor antigos na [!DNL BACKUP/] pasta.

1. Quando a instalação estiver concluída, clique em &quot;Concluir&quot; para sair do assistente de instalação.

   Em alguns casos, o assistente de instalação pode solicitar a reinicialização do sistema.

Durante uma atualização, o [!DNL ImageServing/conf/server.xml] arquivo é atualizado para as configurações mais recentes. Se você alterou ou adicionou algum valor, salve o existente [!DNL server.xml] e reimplemente as alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de colocar o servidor em funcionamento. Consulte a descrição do `playlog` utilitário para obter detalhes.
