---
title: Atualização do IS 4.7.4 ou posterior
description: Use esse procedimento ao atualizar o Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Atualização do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use esse procedimento ao atualizar o Dynamic Media Image Serving.

Se estiver atualizando de uma versão mais antiga do Image Serving, entre em contato com o suporte para obter o processo correto.

>[!NOTE]
>
>O [!DNL webapps] pode ser excluída na atualização. Faça o backup do [!DNL webapps] pasta antes da atualização.

1. Faça logon no host do servidor com privilégios administrativos.
1. Extraia o conteúdo do arquivo zip de distribuição do Serviço de Imagens.
1. Inicie o assistente de instalação executando `setup/setup.exe`.
1. Selecionar **[!UICONTROL Next]** para avançar para o Contrato de Licença de Usuário Final (EULA), leia o contrato de licença e selecione **[!UICONTROL Yes]**.

   A próxima página exibe as configurações anteriores.
1. Clique em **[!UICONTROL Next]** para iniciar a instalação de atualização.

   >[!NOTE]
   >
   >O instalador faz o backup dos arquivos de configuração do servidor antigos no [!DNL BACKUP/] pasta.

1. Após a conclusão da instalação, selecione **[!UICONTROL Finish]** para sair do assistente de instalação.

   Às vezes, o assistente de instalação pode solicitar que você reinicialize o sistema.

Durante uma atualização, a variável [!DNL ImageServing/conf/server.xml] O arquivo é atualizado para as configurações mais recentes. Se você alterou ou adicionou valores, deve salvar os valores existentes [!DNL server.xml] e reimplemente suas alterações após a atualização.

Após uma instalação de atualização, considere o aquecimento do cache de resposta HTTP antes de colocar o servidor ativo. Consulte a descrição do `playlog` para obter detalhes.
