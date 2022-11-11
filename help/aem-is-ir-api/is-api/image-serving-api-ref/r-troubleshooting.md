---
description: Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.
solution: Experience Manager
title: Solução de problemas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Solução de problemas{#troubleshooting}

Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.

**Geral**

O ImageServer agora mantém um registro de instalação e uma pasta de backup de todos os arquivos alterados durante uma instalação de atualização. Esse arquivo e a pasta podem ser encontrados na raiz do diretório de instalação do Image Serving.

**Ao iniciar o Servidor de imagem, o script de inicialização é interrompido com a mensagem &quot;iniciar pendente&quot; (somente LINUX)**

Isso pode indicar um problema com a Licença de Exibição de Imagens, como um arquivo de licença ausente ou uma licença temporária expirada. Um arquivo de licença válido deve estar localizado em [!DNL /usr/local/scene7/licenses].

**O Servidor de Imagens interrompe ou falha e o arquivo de log do Servidor de Imagens indica não espaço suficiente ou &quot;recurso temporariamente indisponível no arquivo&quot; [!DNL IgcVirtualMemory.cpp]&quot;**

O motivo para esta mensagem de erro é que o Servidor de Imagens não conseguiu alocar a quantidade de memória que foi configurada para utilizar.

* Verifique a configuração da memória física em [!DNL ImageServerRegistry.xml]. Não deve ser mais do que 50%, menos se outros aplicativos com uso intenso de memória estiverem sendo executados no mesmo sistema. O padrão é 20%.
* Certifique-se de que o espaço de troca no servidor seja pelo menos o dobro do tamanho da RAM física. Configurações de espaço de troca baixo podem causar esse problema.

**O espaço em disco real usado pela pasta de cache excede ` *[!DNL cache.maxSize]*`definido em[!DNL PlatformServer.conf]**

Isso não indica um problema. A sobrecarga do sistema de arquivos não está incluída no [!DNL Platform Server]Configuração do cache de disco do. O montante total reportado pelo sistema pode ser substancialmente superior ao valor fixado. Recomenda-se reservar duas vezes mais espaço em disco do que o especificado em ` *[!DNL cache.maxSize]*`.

**Imagens quebradas nos exemplos de is-docs**

Isso ocorre se o Servidor de imagem não estiver em execução. Também ocorre se o caminho raiz do catálogo ou o caminho raiz da imagem tiverem sido alterados do padrão de instalação, mas as imagens e catálogos de exemplo não foram movidos para os novos locais. Verifique o valor do Caminho Raiz do Servidor de Imagens nos arquivos de configuração. Se necessário, mova a pasta de demonstração que contém as imagens de exemplo para a raiz da imagem atual e mova [!DNL sample*.*] à raiz de catálogo atual.

Os exemplos também presumem que determinadas configurações em [!DNL default.ini] são padrão (por exemplo, a ofuscação ou o bloqueio não devem ser ativados).

**Demasiadas falhas de cache após um tempo de atividade substancial**

Dependendo do uso do servidor, o desempenho pode ser melhorado com o aumento [!DNL Platform Server] tamanho do cache de disco se houver espaço disponível. As configurações podem ser alteradas editando manualmente os arquivos de configuração. Consulte a documentação.

**Os arquivos de log estão ocupando muito espaço em disco**

O servidor de imagem e [!DNL Platform Server] inicie um novo arquivo de log todos os dias. Por padrão, eles são colocados no [!DNL *[!DNL install_root]*/ImageServing/logs]. Tamanho do arquivo de log, número de logs mantidos e o conteúdo do log pode ser configurado. Consulte a documentação.

**Se tiver software antivírus instalado no servidor**

É recomendável desativar a verificação para diretórios do Image Serving. Caso contrário, a varredura de diretórios de leitura/gravação de alto volume (como cache, imagens, fontes, perfis e diretórios de catálogo) causará problemas.

**Digimarc causa problemas de desempenho para imagens de zoom**

Não use Digimarc em imagens com zoom. O desempenho não será aceitável. Se necessário, crie um catálogo separado para as imagens a serem usadas no zoom e desative o Digimarc para este catálogo.
