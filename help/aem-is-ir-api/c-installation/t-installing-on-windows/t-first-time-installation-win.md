---
description: Use estas etapas para instalar o Image Serving pela primeira vez no Windows.
solution: Experience Manager
title: Instalação pela primeira vez
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# Instalar pela primeira vez{#installing-for-the-first-time}

Use estas etapas para instalar o Image Serving pela primeira vez no Windows.

1. Faça logon no host do servidor com privilégios administrativos.
1. Se já tiver recebido uma licença, copie-a para o seu servidor e execute a instalação da licença clicando duas vezes no arquivo.

   Se você ainda não tiver uma licença, poderá continuar com a instalação e instalar a licença posteriormente.
1. Extraia o conteúdo do arquivo zip de distribuição do Serviço de Imagens.
1. Execute [!DNL setup]/ [!DNL setup.exe] para iniciar o assistente de instalação.
1. Clique em &quot;Avançar&quot; para avançar para o Contrato de Licença de Usuário Final (EULA), leia o contrato de licença e clique em **[!UICONTROL Yes]**.

   A caixa de diálogo [!DNL Authentication] é exibida em seguida.
1. Se uma licença já estiver instalada e as informações da licença aparecerem na caixa de diálogo [!DNL Authentication], clique em **[!UICONTROL Next]** para continuar.

   Se você não tiver uma licença, clique em **[!UICONTROL Request License]**. A próxima caixa de diálogo mostra um dos endereços MAC da Placa de Interface de Rede da sua máquina. Envie um email para este endereço MAC, o nome da empresa e o produto que você está instalando, conforme determinado pelo prompt.

   **Importante:** a licença se baseia no endereço MAC de uma das Placas de Interface de Rede instaladas nesse host. Se desativar, remover ou substituir este cartão, a licença deixará de ser reconhecida como válida. Certifique-se de obter uma licença para a configuração de hardware que você usará para IS.

   Pode continuar a instalar o IS sem uma licença válida e instalar a licença mais tarde. Para continuar, clique em **[!UICONTROL Back]** para retornar à caixa de diálogo [!DNL Authentication] e clique em **[!UICONTROL Next]**.
1. Vá para a página &quot;Configurações do administrador do servidor da plataforma&quot;. Insira novos valores conforme necessário ou aceite os padrões.

   Você pode configurar os seguintes itens:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Porta de Conexão HTTP do Servidor da Plataforma </p> </td> 
   <td> <p>Porta de escuta HTTP principal para disponibilização de imagens e processamento de imagens </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Porta de escuta do administrador </p> </td> 
   <td> <p>Porta de escuta do administrador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Tamanho do Cache do Servidor da Plataforma em MB </p> </td> 
   <td> <p>Tamanho inicial do cache de resposta principal </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Localização do Cache do Servidor de Plataforma </p> </td> 
   <td> <p>Pasta de cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

Os números de porta especificados devem ser exclusivos e não devem ser usados por outros aplicativos ou serviços.

A próxima tela fornece uma oportunidade para analisar as configurações selecionadas.
1. Clique em **[!UICONTROL Back]** para fazer alterações ou clique em **[!UICONTROL Next]** para iniciar a instalação.
1. Clique em **[!UICONTROL Finish]** para sair do assistente de instalação.
