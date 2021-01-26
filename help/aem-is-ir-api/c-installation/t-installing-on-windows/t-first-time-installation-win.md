---
description: Use estas etapas para instalar o Serviço de imagem pela primeira vez no Windows.
seo-description: Use estas etapas para instalar o Serviço de imagem pela primeira vez no Windows.
seo-title: Instalação pela primeira vez
solution: Experience Manager
title: Instalação pela primeira vez
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Instalação pela primeira vez{#installing-for-the-first-time}

Use estas etapas para instalar o Serviço de imagem pela primeira vez no Windows.

1. Faça logon no host do servidor com privilégios administrativos.
1. Se você já tiver recebido uma licença, copie-a para seu servidor e execute a instalação da licença clicando no duplo.

   Se você ainda não tiver uma licença, poderá continuar com a instalação e instalar a licença mais tarde.
1. Extraia o conteúdo do arquivo zip de distribuição do Servidor de imagens.
1. Execute [!DNL setup]/ [!DNL setup.exe] para iniciar o assistente de instalação.
1. Clique em &quot;Avançar&quot; para avançar até o Contrato de Licença de Usuário Final (EULA), ler o contrato de licença e clicar em **[!UICONTROL Yes]**.

   A caixa de diálogo [!DNL Authentication] será exibida em seguida.
1. Se uma licença já estiver instalada e as informações da licença forem exibidas na caixa de diálogo [!DNL Authentication], clique em **[!UICONTROL Next]** para continuar.

   Se você não tiver uma licença, clique em **[!UICONTROL Request License]**. A caixa de diálogo seguinte mostra um dos endereços MAC da placa de interface de rede do seu computador. Envie este endereço MAC por e-mail, seu nome de empresa e o produto que você está instalando, conforme indicado pelo prompt.

   **Importante:** a licença se baseia no endereço MAC de uma das placas de interface de rede instaladas nesse host. Se você desativar, remover ou substituir este cartão, a licença não será mais reconhecida como válida. Certifique-se de obter uma licença para a configuração de hardware que você usará para IS.

   Você pode continuar instalando o IS sem uma licença válida e instalar a licença mais tarde. Para continuar, clique em **[!UICONTROL Back]** para retornar à caixa de diálogo [!DNL Authentication] e clique em **[!UICONTROL Next]**.
1. Vá para a página &quot;Configurações de administrador do servidor da plataforma&quot;. Insira novos valores conforme necessário ou aceite os padrões.

   Você pode configurar os seguintes itens:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> Porta de conexão HTTP do servidor da plataforma </p> </td> 
   <td> <p>Porta de escuta HTTP principal para o serviço de imagem e renderização de imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Porta de escuta do administrador </p> </td> 
   <td> <p>Porta de escuta do administrador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Tamanho do cache do servidor da plataforma em MB </p> </td> 
   <td> <p>Tamanho inicial do cache de resposta principal </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Localização do Cache do Servidor da Plataforma </p> </td> 
   <td> <p>Pasta de cache PS </p> </td> 
  </tr> 
 </tbody> 
</table>

Os números de porta especificados devem ser exclusivos e não usados por outros aplicativos ou serviços.

A tela seguinte oferece uma oportunidade de rever as configurações selecionadas.
1. Clique em **[!UICONTROL Back]** para fazer alterações ou clique em **[!UICONTROL Next]** para start da instalação.
1. Clique em **[!UICONTROL Finish]** para sair do assistente de instalação.
