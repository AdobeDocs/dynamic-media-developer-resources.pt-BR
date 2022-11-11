---
title: Instalação pela primeira vez
description: Use estas etapas para instalar o Image Serving pela primeira vez no Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Instalação pela primeira vez{#installing-for-the-first-time}

Use estas etapas para instalar o Image Serving pela primeira vez no Windows.

1. Faça logon no host do servidor com privilégios administrativos.
1. Se já tiver recebido uma licença, copie-a para o seu servidor e execute a instalação da licença clicando duas vezes no arquivo.

   Se você ainda não tiver uma licença, poderá continuar com a instalação e instalar a licença posteriormente.

1. Extraia o conteúdo do arquivo zip de distribuição do Serviço de Imagens.
1. Inicie o assistente de instalação executando [!DNL setup]/ [!DNL setup.exe].
1. Selecionar **[!UICONTROL Next]** para avançar para o Contrato de Licença de Usuário Final (EULA), leia o contrato de licença e selecione **[!UICONTROL Yes]**.

   O [!DNL Authentication] será exibida em seguida.
1. Se uma licença já estiver instalada e as informações da licença aparecerem no [!DNL Authentication] caixa de diálogo, selecione **[!UICONTROL Next]** para continuar.

   Se não tiver uma licença, selecione **[!UICONTROL Request License]**. A próxima caixa de diálogo mostra um dos endereços MAC da placa de interface de rede da sua máquina. Envie um email para este endereço do MAC, o nome da empresa e o produto que você está instalando, conforme determinado pelo prompt.

   **Importante:** A licença é baseada no endereço MAC de uma das placas de interface de rede instaladas nesse host. Se você desativar, remover ou substituir esse cartão, a licença não será mais reconhecida como válida. Certifique-se de obter uma licença para a configuração de hardware usada para o Serviço de Imagens.

   Pode continuar a instalar o IS sem uma licença válida e instalar a licença mais tarde. Para continuar, selecione **[!UICONTROL Back]** para retornar ao [!DNL Authentication] e selecione **[!UICONTROL Next]**.
1. Prossiga para o[!DNL Platform Server] Página &quot;Configurações do administrador&quot;. Insira novos valores conforme necessário ou aceite os padrões.

   Você pode configurar os seguintes itens:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Porta de conexão HTTP </p> </td>
      <td> <p>Porta de escuta HTTP principal para disponibilização de imagens e processamento de imagens </p> </td>
   </tr> 
   <tr> 
      <td> <p> Porta de escuta do administrador </p> </td>
      <td> <p>Porta de escuta do administrador </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] Tamanho do Cache em MB </p> </td>
      <td> <p>Tamanho inicial do cache de resposta principal </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Localização do Cache </p> </td>
      <td> <p>Pasta de cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   Os números de porta especificados devem ser exclusivos e não devem ser usados por outros aplicativos ou serviços.

   A próxima tela fornece uma oportunidade para revisar as configurações selecionadas.

1. Selecionar **[!UICONTROL Back]** para fazer alterações ou selecione **[!UICONTROL Next]** para iniciar a instalação.

1. Selecionar **[!UICONTROL Finish]** para sair do assistente de instalação.
