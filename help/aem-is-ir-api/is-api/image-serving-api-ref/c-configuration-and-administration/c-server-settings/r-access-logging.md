---
description: Use essas configurações do servidor para acessar o registro em log.
seo-description: Use essas configurações do servidor para acessar o registro em log.
seo-title: Log de acesso
solution: Experience Manager
title: Log de acesso
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---


# Log de acesso{#access-logging}

Use essas configurações do servidor para acessar o registro em log.

Sintaxe

## TC::diretory - pasta de arquivos de log {#section-5d9e2168d4504bbe9868b7d6051c9d67}

A pasta na qual o Servidor de plataforma grava arquivos de log. Pode ser um caminho absoluto ou um caminho relativo a *`install_folder`*. O padrão é [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se a pasta tem os privilégios de acesso de leitura/gravação corretos se o Serviço de imagem estiver instalado para ser executado em uma conta de usuário diferente da raiz.

## TC::maxDays - Número de dias para manter arquivos de log {#section-45cbecffc5694c87b7d5c176a44a4885}

O número de dias que os arquivos de log devem ser preservados. Novos arquivos de registro são criados todos os dias à meia-noite. No momento, o servidor excluirá todos os arquivos na pasta do arquivo de log que forem mais antigos que o número especificado de dias, incluindo os gravados pelo Servidor de imagens ou pelo Servidor de renderização. O padrão é 10.

## TC::prefix - Nome do arquivo de log de acesso {#section-1003856323b844049632710a5a056aa7}

Prefixo de nome do arquivo no qual os dados do log de acesso são gravados. A data e o sufixo do arquivo ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) são anexados à string especificada. O nome do arquivo de log de acesso deve ser diferente do do arquivo de log de rastreamento. O padrão é &quot; `access-`&quot;.

## TC::pattern - Padrão de registro de acesso {#section-22775ea85cee444d8a7d7336a3b1feef}

Especifica o padrão de dados para registros de log de acesso do Servidor de Plataformas. A string de padrão especifica variáveis que são substituídas pelos valores correspondentes. Todos os outros caracteres na string de padrão são transferidos literalmente para o registro de log.

Para usar o utilitário de aquecimento do cache, os espaços devem ser usados como separadores de campos. O Servidor de plataforma substitui todos os espaços e caracteres &#39;%&#39; nos valores de campo por `%20` e `%25`, respectivamente.

As seguintes variáveis de padrão são suportadas:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Padrão</b> </th> 
   <th class="entry"> <b>Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a  </span> </p> </td> 
   <td> <p>Endereço IP remoto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A  </span> </p> </td> 
   <td> <p>Endereço IP local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b  </span> </p> </td> 
   <td> <p>Contagem de bytes de resposta excluindo cabeçalhos HTTP, ou ' ' se zero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B  </span> </p> </td> 
   <td> <p>Contagem de bytes de resposta excluindo cabeçalhos HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D  </span> </p> </td> 
   <td> <p>Tempo de processamento da solicitação em milissegundos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I  </span> </p> </td> 
   <td> <p>id de thread (para fazer referência cruzada às entradas de depuração/log de erros). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G  </span> </p> </td> 
   <td> <p>data e hora, formatadas como <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> Deslocamento  </span> do SSS  </span> </p> <p> ( <span class="varname"> SSS </span> são msec, <span class="varname"> deslocamento </span> é o deslocamento de tempo GMT); o valor de hora é capturado quando a resposta é enviada para o cliente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m  </span> </p> </td> 
   <td> <p>Método de solicitação ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> e assim por diante). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O  </span> </p> </td> 
   <td> <p>Sobreposição de solicitações (número de solicitações processadas simultaneamente). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p  </span> </p> </td> 
   <td> <p>Porta local na qual esta solicitação foi recebida. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q  </span> </p> </td> 
   <td> <p>Sequência de caracteres do query (precedida por um '?' se existir). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r  </span> </p> </td> 
   <td> <p>Primeira linha de solicitação (método de solicitação, URI, versão HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R  </span> </p> </td> 
   <td> <p>Igual a <span class="codeph"> %r </span>, mas aplica codificação HTTP limitada ao URI para evitar problemas de análise de log. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s  </span> </p> </td> 
   <td> <p>Código de status da resposta HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S  </span> </p> </td> 
   <td> <p>ID da sessão do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t  </span> </p> </td> 
   <td> <p>Data e hora, em Formato de log comum. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u  </span> </p> </td> 
   <td> <p>Usuário remoto autenticado (se houver), senão ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U  </span> </p> </td> 
   <td> <p>Caminho URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v  </span> </p> </td> 
   <td> <p>Nome do servidor local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T  </span> </p> </td> 
   <td> <p>Tempo de processamento da solicitação em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Chave de cache do Servidor de plataforma (pasta/nome do arquivo de cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Palavra-chave de gerenciamento de cache do Platform Server: <span class="codeph"> { REUSED | CRIADO | ATUALIZADO | REMOTO | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDADO | IGNORADO | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>O tipo MIME da resposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>O contexto de destino se ocorrer um contexto adiante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>O valor do cabeçalho de resposta <span class="codeph"> etag </span> (assinatura MD5 dos dados de resposta). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Mensagem de erro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Tempo necessário para recuperar a entrada ou os dados do cache do Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Tempo gasto para a análise de solicitação e pesquisa de catálogo de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Indica se esta solicitação tentou ou não qualquer acesso baseado em caminho fora do sistema de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>O endereço IP do servidor peer no cluster de cache que forneceu a entrada do cache ou '-' se <span class="codeph"> CacheUse </span> não for <span class="codeph"> REMOTE_CREATED </span> nem <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Categoria de erro: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=sem erro. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=imagem(ões) não encontrada(s) no servidor. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=Erro de uso do protocolo IS ou erro de conteúdo diferente de 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=outro erro de servidor. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=solicitação recusada devido à sobrecarga temporária do servidor. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>O valor em maiúsculas de <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>A ID raiz do catálogo principal da solicitação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>O tempo necessário para o Servidor de plataforma enviar a resposta após a gravação de dados para o fluxo de saída. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Como <span class="codeph"> %B </span>, mas inclui valores para respostas 304 (não modificadas). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformationUrl}r  </span> </p> </td> 
   <td> <p>O URL final após todas as transformações do conjunto de regras. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>O valor do cabeçalho de solicitação HTTP especificado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>O valor do cabeçalho de resposta HTTP especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

O padrão é `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
