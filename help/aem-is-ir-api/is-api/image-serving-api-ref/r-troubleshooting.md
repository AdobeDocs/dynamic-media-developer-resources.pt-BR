---
description: Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.
seo-description: Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.
seo-title: Solução de problemas
solution: Experience Manager
title: Solução de problemas
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---


# Solução de problemas{#troubleshooting}

Esta seção contém soluções para problemas que ocasionalmente ocorreram com o Serviço de imagem.

**Geral**

O ImageServer agora mantém um registro de instalação e uma pasta de backup de todos os arquivos alterados durante uma instalação de atualização. Este arquivo e pasta podem ser encontrados na raiz do diretório de instalação do Servidor de imagens.

**Ao iniciar o Servidor de imagens, o script de inicialização pára com a mensagem &quot;start pendente&quot; (somente LINUX)**

Isso pode indicar um problema com a Licença de disponibilização de imagem, como um arquivo de licença ausente ou uma licença temporária expirada. Um arquivo de licença válido deve estar localizado em [!DNL /usr/local/scene7/licenses].

**O Servidor de imagens pára ou trava e o arquivo de log do Servidor de imagens indica que não há espaço suficiente ou &quot;recurso temporariamente indisponível no arquivo  [!DNL IgcVirtualMemory.cpp]&quot;**

O motivo desta mensagem de erro é que o Servidor de imagens não conseguiu alocar a quantidade de memória que foi configurada para utilizar.

* Verifique a configuração de memória física em [!DNL ImageServerRegistry.xml]. Não deve ser mais que 50%, menos se outros aplicativos com uso intenso de memória estiverem em execução no mesmo sistema. O padrão é 20%.
* Verifique se o espaço de troca no servidor tem pelo menos duplo tamanho de RAM física. As configurações de pouco espaço de troca podem causar esse problema.

**O espaço em disco real usado pela pasta de cache excede o  ` *[!DNL cache.maxSize]*`definido em[!DNL PlatformServer.conf]**

Isso não indica um problema. A sobrecarga do sistema de arquivos não está incluída na configuração de cache de disco do Servidor de plataforma. O montante total reportado pelo sistema pode ser substancialmente superior ao valor definido. É recomendável reservar o dobro do espaço em disco especificado em ` *[!DNL cache.maxSize]*`.

**Imagens quebradas nos exemplos de is-docs**

Isso ocorre se o Servidor de imagens não estiver sendo executado. Também ocorre se o caminho raiz do catálogo ou o caminho raiz da imagem tiver sido alterado do padrão de instalação, mas as imagens e catálogos de exemplo não tiverem sido movidos para os novos locais. Verifique o valor do Caminho raiz do servidor de imagens nos arquivos de configuração. Se necessário, mova a pasta de demonstração que contém as imagens de exemplo para a raiz da imagem atual e mova [!DNL sample*.*] para a raiz do catálogo atual.

Os exemplos também presumem que determinadas configurações em [!DNL default.ini] são padrão (por exemplo, ofuscação ou bloqueio não devem ser ativados).

**Demasiadas falhas de cache após um tempo de funcionamento substancial**

Dependendo do uso do servidor, o desempenho pode ser melhorado aumentando o tamanho do cache de disco do Platform Server se houver espaço em disco disponível. As configurações podem ser alteradas editando manualmente os arquivos de configuração. Consulte a documentação.

**Os arquivos de registro estão ocupando muito espaço em disco**

O Servidor de imagens e o Servidor de plataformas start um novo arquivo de log todos os dias. Por padrão, eles são colocados em [!DNL *[!DNL install_root]*/ImageServing/logs]. Tamanho do arquivo de log, número de logs mantidos e conteúdo de log pode ser configurado. Consulte a documentação.

**Se você tiver um software antivírus instalado no servidor**

É recomendável desativar a varredura para diretórios do Servidor de imagens. Caso contrário, a digitalização de diretórios de leitura/gravação de alto volume (como cache, imagens, fontes, perfis e diretórios de catálogo) causará problemas.

**A Digimarc causa problemas de desempenho para imagens de zoom**

Não utilize Digimarc em imagens com zoom. O desempenho não será aceitável. Se necessário, crie um catálogo separado para as imagens a serem usadas para aplicar zoom e desative a Digimarc para este catálogo.
