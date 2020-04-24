---
description: Esta documentação explica como administrar o servidor de renderização de imagem do Scene7.
seo-description: Esta documentação explica como administrar o servidor de renderização de imagem do Scene7.
seo-title: Visão geral da administração do servidor
solution: Experience Manager
title: Visão geral da administração do servidor
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Visão geral da administração do servidor{#server-administration-overview}

Esta documentação explica como administrar o servidor de renderização de imagem do Scene7.

A renderização de imagem consiste em dois componentes principais:

* Um pacote Java é implantado com o Servidor da plataforma de disponibilização de imagens e gerencia a conexão do cliente, o armazenamento em cache e catálogos de materiais.
* Um módulo de código nativo é implantado como uma biblioteca de extensão para o Servidor de imagens e implementa as funcionalidades principais de renderização de imagens.

Ambos os componentes são chamados coletivamente de Servidor *de* renderização.

A Renderização de imagem compartilha vários recursos do servidor com o Serviço de imagem e todas as opções são configuradas pela edição de um arquivo de configuração. Os atributos de configuração adicionais são fornecidos pelo catálogo padrão ( [!DNL default.ini]) ou catálogos de materiais específicos. Consulte Catálogos de materiais para obter detalhes.

A pasta de instalação de renderização de imagem ( *[!DNL install_folder]*) é [!DNL *[!DNL install_root]*/ImageRendering]. No Windows, o padrão *[!DNL install_root]* é `C:\Program Files\Scene7`. Uma pasta diferente pode ser especificada durante a instalação. No Linux, *[!DNL install_root]* deve ser sempre [!DNL /usr/local/scene7]. Podem ser utilizados links simbólicos.

Todos os caminhos de arquivo fazem distinção entre maiúsculas e minúsculas no UNIX e não fazem distinção entre maiúsculas e minúsculas no Windows.
