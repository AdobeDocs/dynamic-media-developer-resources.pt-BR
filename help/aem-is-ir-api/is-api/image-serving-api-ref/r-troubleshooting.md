---
description: Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.
seo-description: Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.
seo-title: Solução de problemas
solution: Experience Manager
title: Solução de problemas
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---


# Solução de problemas{#troubleshooting}

Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.

**Geral**

O ImageServer agora mantém um registro de instalação e uma pasta de backup de todos os arquivos alterados durante uma instalação de atualização. Esse arquivo e a pasta podem ser encontrados na raiz do diretório de instalação do Image Serving.

**Ao iniciar o Servidor de imagem, o script de inicialização é interrompido com a mensagem &quot;iniciar pendente&quot; (somente LINUX)**

Isso pode indicar um problema com a Licença de Exibição de Imagens, como um arquivo de licença ausente ou uma licença temporária expirada. Um arquivo de licença válido deve estar localizado em [!DNL /usr/local/scene7/licenses].

**O Servidor de Imagens interrompe ou falha e o arquivo de log do Servidor de Imagens indica não espaço suficiente ou &quot;recurso temporariamente indisponível no arquivo  [!DNL IgcVirtualMemory.cpp]&quot;**

O motivo para esta mensagem de erro é que o Servidor de Imagens não conseguiu alocar a quantidade de memória que foi configurada para utilizar.

* Verifique a configuração Memória física em [!DNL ImageServerRegistry.xml]. Não deve ser mais do que 50%, menos se outros aplicativos com uso intenso de memória estiverem sendo executados no mesmo sistema. O padrão é 20%.
* Certifique-se de que o espaço de troca no servidor seja pelo menos o dobro do tamanho da RAM física. Configurações de espaço de troca baixo podem causar esse problema.

**O espaço em disco real usado pela pasta de cache excede o  ` *[!DNL cache.maxSize]*`definido em[!DNL PlatformServer.conf]**

Isso não indica um problema. A sobrecarga do sistema de arquivos não está incluída na configuração de cache de disco do Servidor de Plataforma. O montante total reportado pelo sistema pode ser substancialmente superior ao valor fixado. É recomendável reservar duas vezes mais espaço em disco do que é especificado em ` *[!DNL cache.maxSize]*`.

**Imagens quebradas nos exemplos de is-docs**

Isso ocorre se o Servidor de imagem não estiver em execução. Também ocorre se o caminho raiz do catálogo ou o caminho raiz da imagem tiverem sido alterados do padrão de instalação, mas as imagens e catálogos de exemplo não foram movidos para os novos locais. Verifique o valor do Caminho Raiz do Servidor de Imagens nos arquivos de configuração. Se necessário, mova a pasta de demonstração que contém as imagens de exemplo para a raiz da imagem atual e mova [!DNL sample*.*] para a raiz do catálogo atual.

Os exemplos também presumem que determinadas configurações em [!DNL default.ini] são padrão (por exemplo, ofuscação ou bloqueio não devem ser ativadas).

**Demasiadas falhas de cache após um tempo de atividade substancial**

Dependendo do uso do servidor, o desempenho pode ser aprimorado aumentando o tamanho do cache de disco do Platform Server se houver espaço em disco disponível. As configurações podem ser alteradas editando manualmente os arquivos de configuração. Consulte a documentação.

**Os arquivos de log estão ocupando muito espaço em disco**

O Servidor de imagem e o Servidor de plataforma iniciam um novo arquivo de log todos os dias. Por padrão, eles são colocados em [!DNL *[!DNL install_root]*/ImageServing/logs]. Tamanho do arquivo de log, número de logs mantidos e o conteúdo do log pode ser configurado. Consulte a documentação.

**Se tiver software antivírus instalado no servidor**

É recomendável desativar a verificação para diretórios do Image Serving. Caso contrário, a varredura de diretórios de leitura/gravação de alto volume (como cache, imagens, fontes, perfis e diretórios de catálogo) causará problemas.

**Digimarc causa problemas de desempenho para imagens de zoom**

Não use o Digimarc em imagens que serão ampliadas. O desempenho não será aceitável. Se necessário, crie um catálogo separado para as imagens a serem usadas no zoom e desative o Digimarc para este catálogo.
