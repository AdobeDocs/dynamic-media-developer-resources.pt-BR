---
title: Instalação pela primeira vez
description: Use essas etapas para instalar o Servidor de imagens pela primeira vez no Windows.
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

Use essas etapas para instalar o Servidor de imagens pela primeira vez no Windows.

1. Efetue login no host do servidor com privilégios administrativos.
1. Se você já tiver recebido uma licença, copie-a no servidor e execute a instalação da licença clicando duas vezes no arquivo.

   Se você ainda não tiver uma licença do, poderá prosseguir com a instalação e instalar a licença mais tarde.

1. Extraia o conteúdo do arquivo zip de distribuição do Servidor de imagens.
1. Inicie o assistente de instalação, executando [!DNL setup]/ [!DNL setup.exe].
1. Selecionar **[!UICONTROL Next]** para avançar para o Contrato de licença de usuário final (EULA), leia o contrato de licença e selecione **[!UICONTROL Yes]**.

   A variável [!DNL Authentication] é exibida a seguir.
1. Se uma licença já estiver instalada e as informações da licença aparecerem no [!DNL Authentication] caixa de diálogo, selecione **[!UICONTROL Next]** para continuar.

   Se você não tiver uma licença, selecione **[!UICONTROL Request License]**. A próxima caixa de diálogo mostra um dos endereços MAC da placa de interface de rede do computador. Envie por email este endereço da MAC, o nome da sua empresa e o produto que você está instalando, conforme indicado no prompt.

   **Importante:** A licença se baseia no endereço MAC de uma das placas de interface de rede instaladas nesse host. Se você desativar, remover ou substituir este cartão, a licença não será mais reconhecida como válida. Certifique-se de obter uma licença para a configuração de hardware usada para o Servidor de imagens.

   Você pode continuar a instalar o IS sem uma licença válida e instalar a licença mais tarde. Para continuar, selecione **[!UICONTROL Back]** para retornar ao [!DNL Authentication] e selecione **[!UICONTROL Next]**.
1. Passe para a página &quot;[!DNL Platform Server] Configurações do administrador&quot;. Insira novos valores, conforme necessário, ou aceite os padrões.

   Você pode configurar os seguintes itens:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Porta de conexão HTTP </p> </td>
      <td> <p>Porta principal de escuta HTTP para o Servidor de imagens e a Renderização de imagens </p> </td>
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
      <td> <p> [!DNL Platform Server] Localização do cache </p> </td>
      <td> <p>Pasta de cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   Os números de porta especificados devem ser exclusivos e não usados por outros aplicativos ou serviços.

   A próxima tela oferece uma oportunidade de revisar as configurações selecionadas.

1. Selecionar **[!UICONTROL Back]** para fazer alterações ou selecione **[!UICONTROL Next]** para iniciar a instalação.

1. Selecionar **[!UICONTROL Finish]** para sair do assistente de instalação.
