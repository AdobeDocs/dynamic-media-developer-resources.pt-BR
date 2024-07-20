---
description: O utilitário playlog pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP.
solution: Experience Manager
title: O utilitário 'playlog'
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# O utilitário &#39;playlog&#39;{#the-playlog-utility}

O utilitário playlog pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP.

O cache de resposta HTTP existente do Servidor de imagens não é utilizável após uma atualização de versão principal (quando o primeiro ou o segundo dígito do número de versão é alterado). Se o servidor precisar ser colocado em condições de carga total após a atualização, o servidor poderá ficar sobrecarregado ao lidar com as primeiras horas de solicitações de perda de cache até que o cache seja razoavelmente preenchido e a taxa de ocorrência do cache aumente.

Para evitar esse pico de carga inicial, o utilitário `playlog` pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP. `playlog` extrai solicitações HTTP de um arquivo de log de acesso existente e o envia ao servidor para gerar entradas de cache. Para cenários de uso típicos, é suficiente reproduzir um único arquivo de log de acesso contendo tráfego de um dia inteiro.

Além de preparar o cache de resposta HTTP após a instalação da atualização, o utilitário também é usado para pré-gerar conteúdo de cache ao adicionar um novo servidor a um ambiente com balanceamento de carga; basta reproduzir um arquivo de log recente de um dos outros servidores.

O `playlog` pode ser configurado para oferecer suporte à maioria dos arquivos de log de acesso gerados por versões anteriores do Servidor de imagens.

## Uso {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> prefixo </span> </span> </p> </td> 
  <td class="stentry"> <p>URL raiz para anexar às solicitações extraídas do arquivo de log. </p> <p>Padrão: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>Número do campo (coluna) que contém a solicitação no registro de log; com base em 1. </p> <p>Padrão: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> separador </span> </span> </p> </td> 
  <td class="stentry"> <p>Separador de campos; padrão de expressão regular. </p> <p>Padrão: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> marcador </span> </span> </p> </td> 
  <td class="stentry"> <p>Marcador de solicitação; identifica solicitações no arquivo de log que devem ser reproduzidas; padrão de expressão regular. </p> <p>Padrão: <span class="codeph"> (Solicitação: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> sufixo </span> </span> </p> </td> 
  <td class="stentry"> <p>Sufixo a ser anexado à solicitação extraída do arquivo de log; pode ser usado para separar solicitações reproduzidas de solicitações ativas nos arquivos de log; um caractere "?" ou o separador '&amp;' é inserido automaticamente; o sufixo pode fazer referência a qualquer campo de log por posição entre chaves. O padrão corresponde ao campo de assinatura md5. </p> <p>Padrão: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>Modo detalhado, imprime as URLs de solicitação geradas em <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Imprimir um resumo para <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>método de solicitação - método de solicitação HTTP a ser usado ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Padrão: <span class="codeph"> inteligente (</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - cole no arquivo de log para capturar o método original do. </p> <p>Padrão: 15 </p> </td> 
 </tr> 
</table>

Para o Windows, o nome do arquivo é [!DNL playlog.bat] e no Linux é [!DNL playlog.sh].

## Exemplos {#section-716e5c35e9fa4ee3a4b0687381fcea40}

O exemplo a seguir reproduz todas as solicitações de um arquivo de log de acesso criado pelo Servidor de imagens no Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

O comando a seguir reproduz todas as solicitações encontradas em um arquivo de log de rastreamento criado pelo Servidor de imagens no Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
