---
title: Atualizando do IS 4.7.4 ou posterior
description: Use este procedimento ao atualizar o Servidor de imagens do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 0%

---

# Atualizando do IS 4.7.4 ou posterior{#updating-from-is-or-later}

Use este procedimento ao atualizar o Servidor de imagens do Dynamic Media.

Se você estiver atualizando de uma versão mais antiga do Servidor de imagens, entre em contato com o suporte para obter o processo correto.

>[!NOTE]
>
>A pasta [!DNL webapps] pode ser excluída na atualização. Faça backup da pasta [!DNL webapps] antes de atualizar.

1. Efetue login no host do servidor com privilégios administrativos.
1. Extraia o conteúdo do arquivo zip de distribuição do Servidor de imagens.
1. Inicie o assistente de instalação executando `setup/setup.exe`.
1. Selecione **[!UICONTROL Next]** para avançar para o Contrato de Licença de Usuário Final (EULA), leia o contrato de licença e selecione **[!UICONTROL Yes]**.

   A próxima página exibe as definições de configuração anteriores.
1. Clique em **[!UICONTROL Next]** para iniciar a instalação da atualização.

   >[!NOTE]
   >
   >O instalador faz backup dos arquivos de configuração do servidor antigo na pasta [!DNL BACKUP/].

1. Após a conclusão da instalação, selecione **[!UICONTROL Finish]** para sair do assistente de instalação.

   Às vezes, o assistente de instalação pode solicitar que você reinicialize o sistema.

Durante uma atualização, o arquivo [!DNL ImageServing/conf/server.xml] é atualizado para as configurações mais recentes. Se você alterou ou adicionou valores, salve o [!DNL server.xml] existente e reimplemente as alterações após a atualização.

Após uma instalação de atualização, considere aquecer o cache de resposta HTTP antes de ativar o servidor. Consulte a descrição do utilitário `playlog` para obter detalhes.
