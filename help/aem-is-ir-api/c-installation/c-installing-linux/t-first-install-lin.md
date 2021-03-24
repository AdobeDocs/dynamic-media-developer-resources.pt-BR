---
description: Este procedimento mostra como instalar o Image Serving pela primeira vez no Linux.
solution: Experience Manager
title: Instalação pela primeira vez
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---


# Instalar pela primeira vez{#installing-for-the-first-time}

Este procedimento mostra como instalar o Image Serving pela primeira vez no Linux.

1. Faça logon no host do servidor com permissões de raiz.
1. Crie a pasta [!DNL /usr/local/scene7/licenses].

   Se o arquivo de chave de licença Image Serving and/or Image Rendering (com o sufixo de arquivo [!DNL .sc8]) estiver disponível, copie-o para essa pasta. Caso contrário, continue com a instalação e instale a chave de licença posteriormente.
1. Descompacte e descompacte o arquivo tar de distribuição do Image Serving.
1. Execute [!DNL ./install-is], localizado na pasta [!DNL Setup], para iniciar o assistente de instalação.

   Se nenhuma chave de licença for encontrada, serão exibidas instruções descrevendo como obter um arquivo de licença. Faça isso neste ponto ou continue com a instalação do Image Serving e instale a chave de licença posteriormente.
1. Quando o Acordo de licença de usuário final (EULA) for exibido, leia o contrato de licença e insira `y` para prosseguir.

   O instalador exibe os prompts listados na tabela a seguir.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta de escuta principal [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Porta de escuta HTTP principal para exibição de imagens e renderização de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta de escuta do administrador [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Porta de escuta do administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Tamanho máximo do cache HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Tamanho inicial do cache de resposta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Pasta raiz do cache [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Pasta de cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do Proprietário do Servidor de Imagens [root]:</span> </p> </td> 
   <td colname="col2"> <p>A conta de usuário na qual os servidores de Exibição de Imagens serão instalados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do Grupo do Servidor de Imagens [raiz]:</span> </p> </td> 
   <td colname="col2"> <p>A conta de grupo na qual os servidores de Exibição de imagem serão instalados. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Pressione **[!UICONTROL Enter]** para aceitar o valor padrão ou especificar um valor diferente.

   Certifique-se de que todos os números de porta especificados são exclusivos e não são usados de outra forma neste host.

   >[!IMPORTANT]
   >
   >Se uma conta diferente de raiz for especificada, verifique se as permissões de acesso para todos os arquivos e pastas que o Servidor de imagem precisa ler e/ou gravar estão configuradas corretamente quando essas pastas são reconfiguradas nos arquivos de configuração.
   >
   >O Serviço de Imagens agora está instalado em [!DNL /usr/local/Scene7/ImageServing]. Determinado conteúdo de Renderização de Imagem é instalado em [!DNL /usr/local/Scene7/ImageRendering].
   >
   >No final da instalação, o assistente de instalação tenta iniciar o Servidor de imagem. Se não for encontrada uma chave de licença válida, o Servidor de Imagens não poderá iniciar. Se houver uma licença válida e o Image Server ainda não estiver sendo inicializado, consulte os arquivos de log.

>[!NOTE]
>
>Se a licença for instalada após a instalação do Image Serving, o Servidor de Imagens deve ser iniciado manualmente antes do uso.
