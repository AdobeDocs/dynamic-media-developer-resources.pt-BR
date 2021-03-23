---
description: O utilitário playlog pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP.
seo-description: O utilitário playlog pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP.
seo-title: O utilitário 'playlog'
solution: Experience Manager
title: O utilitário 'playlog'
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# O utilitário &#39;playlog&#39;{#the-playlog-utility}

O utilitário playlog pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP.

O cache de resposta HTTP de Exibição de Imagem existente não é garantido após uma atualização de versão principal (quando o primeiro ou o segundo dígito do número de versão foi alterado). Se o servidor for incorporado às condições de carregamento completo após a atualização, o servidor poderá ser sobrecarregado, entregando as primeiras horas de solicitações de falha de cache até que o cache seja razoavelmente preenchido e a taxa de ocorrência do cache aumente.

Para evitar esse pico de carga inicial, o utilitário `playlog` pode ser usado para pré-gerar conteúdo para o cache de resposta HTTP. `playlog` extrai solicitações HTTP de um arquivo de log de acesso existente e o envia para o servidor para gerar entradas de cache. Para cenários de uso típicos, é suficiente reproduzir um único arquivo de log de acesso contendo o tráfego de um dia inteiro.

Além de preparar o cache de resposta HTTP após as instalações de atualização, o utilitário também é usado para pré-gerar o conteúdo do cache ao adicionar um novo servidor a um ambiente com balanceamento de carga; basta reproduzir um arquivo de log recente de um dos outros servidores.

`playlog` pode ser configurado para suportar a maioria dos arquivos de log de acesso gerados por versões anteriores do Image Serving.

## Uso {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefixo  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL raiz para anexar como prefixo as solicitações extraídas do arquivo de log. </p> <p>Padrão: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número do campo (coluna) que contém a solicitação no registro de log; Baseado em 1. </p> <p>Padrão: 16º </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> separador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Separador de campos; padrão de expressão regular. </p> <p>Padrão: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marcador  </span> </span> </p> </td> 
  <td class="stentry"> <p>Marcador de solicitação; identifica as solicitações no arquivo de log que devem ser reproduzidas; padrão de expressão regular. </p> <p>Padrão: <span class="codeph"> Solicitação: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> sufixo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sufixo para anexar à solicitação extraída do arquivo de log; podem ser usadas para separar solicitações de reprodução de solicitações ativas nos arquivos de log; um '?' ou o separador '&amp;' é inserido automaticamente; o sufixo pode fazer referência a qualquer campo de log por posição em chaves, o padrão corresponde ao campo de assinatura md5. </p> <p>Padrão: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>Modo detalhado, imprime os URLs de solicitação gerados em <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Imprima uma sinopse para <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r  </span> </p> </td> 
  <td class="stentry"> <p>método de solicitação - método de solicitação HTTP a ser usado ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Padrão: <span class="codeph"> inteligente </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o  </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos no arquivo de log para capturar o método original. </p> <p>Padrão: 15. </p> </td> 
 </tr> 
</table>

Para Windows, o nome do arquivo é [!DNL playlog.bat] e no Linux é [!DNL playlog.sh].

## Exemplos {#section-716e5c35e9fa4ee3a4b0687381fcea40}

O exemplo a seguir reproduz todas as solicitações de um arquivo de log de acesso criado pelo Image Serving no Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

O comando a seguir reproduz todas as solicitações encontradas em um arquivo de log de rastreamento criado pelo Serviço de Imagens no Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
