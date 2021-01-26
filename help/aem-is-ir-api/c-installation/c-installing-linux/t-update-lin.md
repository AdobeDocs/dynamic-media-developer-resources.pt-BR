---
description: Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux.
seo-description: Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux.
seo-title: Atualização do IS 4.7.4 ou posterior
solution: Experience Manager
title: Atualização do IS 4.7.4 ou posterior
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Dynamic Media Image Serving no Linux.

Se você estiver atualizando de uma versão mais antiga do Serviço de imagem, entre em contato com o suporte para o processo correto.

A pasta [!DNL webapps] pode ser excluída na atualização. Faça backup da pasta [!DNL webapps] antes da atualização.

1. Faça logon no host do servidor com privilégios de raiz.
1. Descompacte e descompacte o arquivo tar de distribuição do Servidor de imagens.
1. Execute [!DNL ./install-is] para iniciar o assistente de instalação localizado na pasta [!DNL setup].

   O instalador da atualização verifica a integridade e a versão do pacote instalado. Se bem-sucedido, o Contrato de Licença de Usuário Final (&quot;EULA&quot;) será exibido.
1. Leia o contrato de licença e digite &quot;**[!UICONTROL y]**&quot; para prosseguir com a instalação.

   O instalador faz o backup dos arquivos de configuração do servidor antigos na pasta [!DNL BACKUP/].

   Quando a instalação estiver concluída, a seguinte mensagem será exibida:

   `Image Server was started successfully`

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou quaisquer valores, deve salvar [!DNL server.xml] e reimplementar as alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de colocar o servidor em funcionamento. Consulte a descrição do utilitário [!DNL playlog] para obter detalhes.
