---
title: Instalação pela primeira vez
description: Este procedimento mostra como instalar o Servidor de imagens pela primeira vez no Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Instalação pela primeira vez{#installing-for-the-first-time}

Este procedimento mostra como instalar o Servidor de imagens pela primeira vez no Linux®.

1. Faça logon no host do servidor com permissões raiz.
1. Criar a pasta [!DNL /usr/local/scene7/licenses].

   Se o arquivo de chave de licença do Servidor de imagens e/ou Renderização de imagens (com [!DNL .sc8] sufixo do arquivo) estiver disponível, copie-o para esta pasta. Caso contrário, continue com a instalação e instale a chave de licença mais tarde.
1. Descompacte e descompacte o arquivo tar de distribuição do Servidor de imagens.
1. No [!DNL Setup] , inicie o assistente de instalação executando [!DNL ./install-is].

   Se nenhuma chave de licença for encontrada, serão exibidas instruções descrevendo como obter um arquivo de licença. Faça isso neste ponto ou prossiga com a instalação do Servidor de imagens e instale a chave de licença mais tarde.
1. Quando o Contrato de licença de usuário final (EULA) for exibido, leia o contrato de licença e insira `y` para continuar.

   O instalador exibe os prompts listados na tabela a seguir.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta de escuta principal [8080]:</span> </p> </td>
   <td colname="col2"> <p>Porta principal de escuta HTTP para o Servidor de imagens e a Renderização de imagens. </p> </td>
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
   <td colname="col1"> <p><span class="codeph"> Pasta raiz do cache [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Pasta de cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do proprietário do servidor de imagens [root]:</span> </p> </td>
   <td colname="col2"> <p>A conta de usuário na qual o servidor do Servidor de imagens será instalado. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID do grupo do servidor de imagens [root]:</span> </p> </td>
   <td colname="col2"> <p>A conta de grupo na qual o servidor do Servidor de imagens será instalado. </p> </td>
  </tr>
 </tbody>
</table>

1. Pressione **[!UICONTROL Enter]** para aceitar o valor padrão ou especificar um valor diferente.

   Certifique-se de que todos os números de porta especificados sejam exclusivos e não sejam usados neste host.

   >[!IMPORTANT]
   >
   >Se uma conta diferente da raiz for especificada, verifique se as permissões de acesso para todos os arquivos e pastas que o Servidor de imagens precisa para ler e gravar estão configuradas corretamente quando essas pastas forem reconfiguradas nos arquivos de configuração.
   >
   >O Servidor de imagens agora está instalado no [!DNL /usr/local/Scene7/ImageServing]. Determinados conteúdos de Renderização de imagem são instalados no [!DNL /usr/local/Scene7/ImageRendering].
   >
   >No final da instalação, o assistente de instalação tenta iniciar o Servidor de imagens. Se nenhuma chave de licença válida for encontrada, o Servidor de imagens não poderá ser iniciado. Se houver uma licença válida e o Servidor de imagens ainda não estiver sendo inicializado, consulte os arquivos de log.

>[!NOTE]
>
>Se a licença for instalada após a instalação do Servidor de imagens, ele deverá ser iniciado manualmente antes de ser usado.
