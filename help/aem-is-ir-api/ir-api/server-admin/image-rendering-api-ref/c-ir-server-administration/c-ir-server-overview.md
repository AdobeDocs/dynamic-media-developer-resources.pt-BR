---
description: Esta documentação explica como administrar o servidor de Renderização de imagem do Dynamic Media.
solution: Experience Manager
title: Visão geral da administração do servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Visão geral da administração do servidor{#server-administration-overview}

Esta documentação explica como administrar o servidor de Renderização de imagem do Dynamic Media.

A Renderização de imagem consiste em dois componentes principais:

* Um pacote Java é implantado com o Servidor de imagens [!DNL Platform Server] e gerencia a conexão do cliente, o armazenamento em cache e os catálogos de materiais.
* Um módulo de código nativo é implantado como uma biblioteca de extensões para o Servidor de imagens e implementa as funcionalidades principais de renderização de imagem.

Ambos os componentes são chamados coletivamente de *Servidor de renderização*.

A Renderização de imagem compartilha vários recursos do servidor com o Servidor de imagens, e todas as opções são configuradas ao editar um arquivo de configuração. Atributos de configuração adicionais são fornecidos pelo catálogo padrão ( [!DNL default.ini]) ou de catálogos de materiais específicos. Consulte Catálogos de materiais para obter detalhes.

A pasta de instalação da Renderização de imagem ( *[!DNL install_folder]*) é [!DNL *[!DNL install_root]*/ImageRendering]. No Windows, o padrão *[!DNL install_root]* é `C:\Program Files\Scene7`. Uma pasta diferente pode ser especificada durante a instalação. No Linux, *[!DNL install_root]* deve ser sempre [!DNL /usr/local/scene7]. É possível usar links simbólicos.

Todos os caminhos de arquivos fazem distinção entre maiúsculas e minúsculas no UNIX e no Windows.
