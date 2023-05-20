---
description: Esta seção contém soluções para problemas que ocorreram ocasionalmente no Servidor de imagens.
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

Esta seção contém soluções para problemas que ocorreram ocasionalmente no Servidor de imagens.

**Geral**

O ImageServer agora mantém um log de instalação e uma pasta de backup de todos os arquivos alterados durante uma instalação de atualização. Esse arquivo e pasta podem ser encontrados na raiz do diretório de instalação do Servidor de imagens.

**Ao iniciar o Servidor de imagens, o script de inicialização é interrompido com a mensagem &quot;start pending&quot; (somente LINUX)**

Isso pode indicar um problema com a licença do Servidor de imagens, como um arquivo de licença ausente ou uma licença temporária expirada. Um arquivo de licença válido deve estar localizado em [!DNL /usr/local/scene7/licenses].

**O servidor de imagens pára ou trava e o arquivo de registro do servidor de imagens indica que não há espaço suficiente ou que o recurso está temporariamente indisponível no arquivo [!DNL IgcVirtualMemory.cpp]&quot;**

O motivo para essa mensagem de erro é que o Servidor de imagens falhou ao alocar a quantidade de memória configurada para uso.

* Verifique a configuração de memória física no [!DNL ImageServerRegistry.xml]. Ele não deve ser superior a 50%, a menos se outros aplicativos de uso intensivo de memória estiverem em execução no mesmo sistema. O padrão é 20%.
* Verifique se o espaço de troca no servidor tem pelo menos o dobro do tamanho da RAM física. Configurações de pouco espaço de troca podem causar este problema.

**O espaço real em disco usado pela pasta de cache excede ` *[!DNL cache.maxSize]*`definido em[!DNL PlatformServer.conf]**

Isso não indica um problema. A sobrecarga do sistema de arquivos não está incluída no [!DNL Platform Server]Configuração do cache de disco do. O valor total relatado pelo sistema pode ser substancialmente maior do que o valor definido. É recomendável reservar o dobro do espaço em disco especificado em ` *[!DNL cache.maxSize]*`.

**Imagens quebradas nos exemplos is-docs**

Isso ocorre se o Servidor de imagens não estiver em execução. Também ocorre se o caminho raiz do catálogo ou o caminho raiz da imagem tiver sido alterado em relação ao padrão de instalação, mas as imagens e os catálogos de exemplo não tiverem sido movidos para os novos locais. Verifique o valor do Caminho raiz do servidor de imagens nos arquivos de configuração. Se necessário, mova a pasta de demonstração que contém as imagens de exemplo para a raiz da imagem atual e mova [!DNL sample*.*] à raiz do catálogo atual.

Os exemplos também pressupõem que determinadas configurações em [!DNL default.ini] são padrão (por exemplo, ofuscação ou bloqueio não devem estar ativados).

**Muitos erros de cache após um tempo de atividade substancial**

Dependendo do uso do servidor, o desempenho pode ser melhorado aumentando [!DNL Platform Server] tamanho do cache de disco se houver espaço disponível em disco. As configurações podem ser alteradas ao editar manualmente os arquivos de configuração. Consulte a documentação.

**Os arquivos de log estão ocupando muito espaço em disco**

O Servidor de imagens e [!DNL Platform Server] iniciar um novo arquivo de log todos os dias. Por padrão, eles são colocados em [!DNL *[!DNL install_root]*/ImageServing/logs]. O tamanho do arquivo de log, o número de logs mantidos e o conteúdo do log podem ser configurados. Consulte a documentação.

**Se você tiver um software antivírus instalado no servidor**

É recomendável desativar a verificação de diretórios do Servidor de imagens. Caso contrário, a varredura de diretórios de leitura/gravação de alto volume (como cache, imagens, fontes, perfis e diretórios de catálogo) causará problemas.

**A Digimarc causa problemas de desempenho para imagens com zoom**

Não use a Digimarc em imagens com zoom. O desempenho não será aceitável. Se necessário, crie um catálogo separado para imagens a serem usadas para aplicar zoom e desative a Digimarc para esse catálogo.
