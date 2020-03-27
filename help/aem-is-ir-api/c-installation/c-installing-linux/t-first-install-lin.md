---
description: Este procedimento mostra como instalar o Serviço de imagem pela primeira vez no Linux.
seo-description: Este procedimento mostra como instalar o Serviço de imagem pela primeira vez no Linux.
seo-title: Instalação pela primeira vez
solution: Experience Manager
title: Instalação pela primeira vez
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Instalação pela primeira vez{#installing-for-the-first-time}

Este procedimento mostra como instalar o Serviço de imagem pela primeira vez no Linux.

1. Faça logon no host do servidor com permissões de raiz.
1. Crie a pasta [!DNL /usr/local/scene7/licenses].

   Se o arquivo de chave de licença do Servidor de imagens e/ou Renderização de imagens (com sufixo de [!DNL .sc8] arquivo) estiver disponível, copie-o para esta pasta. Caso contrário, continue com a instalação e instale a chave de licença mais tarde.
1. Descompacte e descompacte o arquivo tar de distribuição do Servidor de imagens.
1. 
   4. Execute [!DNL ./install-is], localizado na [!DNL Setup] pasta, para iniciar o assistente de instalação.
   Se nenhuma chave de licença for encontrada, serão exibidas instruções descrevendo como obter um arquivo de licença. Faça isso neste ponto ou prossiga com a instalação do Serviço de imagens e instale a chave de licença mais tarde.
1. Quando o Contrato de Licença de Usuário Final (EULA) for exibido, leia o contrato de licença e digite `y` para prosseguir.

   O instalador exibe os prompts listados na tabela a seguir.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta de escuta principal [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Porta de escuta HTTP principal para o serviço de imagem e renderização de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta de escuta do administrador [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Porta de escuta do administrador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Tamanho Máximo do Cache HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Tamanho inicial do cache de resposta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Pasta raiz de cache [/usr/local/scenen7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Pasta de cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do proprietário do servidor de imagens [raiz]:</span> </p> </td> 
   <td colname="col2"> <p>A conta de usuário na qual os servidores do Servidor de imagens serão instalados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do grupo do servidor de imagens [raiz]:</span> </p> </td> 
   <td colname="col2"> <p>A conta de grupo na qual os servidores de Servidor de imagens serão instalados. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Pressione **[!UICONTROL Enter]** para aceitar o valor padrão ou especificar um valor diferente.

   Certifique-se de que todos os números de porta especificados sejam exclusivos e não usados de outra forma neste host.

   **Importante: **Se uma conta que não seja raiz for especificada, verifique se as permissões de acesso para todos os arquivos e pastas que o Servidor de imagens precisa ler e/ou gravar estão configuradas corretamente quando essas pastas forem reconfiguradas nos arquivos de configuração.
>O Serviço de imagem agora está instalado em [!DNL /usr/local/Scene7/ImageServing]. Determinados conteúdos de renderização de imagem estão instalados em [!DNL /usr/local/Scene7/ImageRendering].
>
>No final da instalação, o assistente de instalação tenta start do Image Server. Se nenhuma chave de licença válida for encontrada, o Servidor de Imagens não poderá start. Se houver uma licença válida e o Servidor de imagens ainda não estiver inicializando, consulte os arquivos de registro.
>[!NOTE]
Se a licença for instalada após a instalação do Servidor de imagens, o Servidor de imagens deverá ser iniciado manualmente antes do uso.
>
>
>

