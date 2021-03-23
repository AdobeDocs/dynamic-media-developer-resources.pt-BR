---
description: Esta documentação explica como administrar o servidor de renderização de imagem do Dynamic Media.
seo-description: Esta documentação explica como administrar o servidor de renderização de imagem do Dynamic Media.
seo-title: Visão geral da administração do servidor
solution: Experience Manager
title: Visão geral da administração do servidor
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# Visão geral da administração do servidor{#server-administration-overview}

Esta documentação explica como administrar o servidor de renderização de imagem do Dynamic Media.

A Renderização de imagem consiste em dois componentes principais:

* Um pacote Java é implantado com o Servidor da plataforma de disponibilização de imagens e gerencia a conexão do cliente, o armazenamento em cache e catálogos de materiais.
* Um módulo de código nativo é implantado como uma biblioteca de extensão para o Servidor de imagem e implementa as funcionalidades principais de renderização de imagem.

Ambos os componentes são chamados coletivamente de *Servidor de renderização*.

A Renderização de imagem compartilha muitas instalações de servidor com o Serviço de imagem e todas as opções são configuradas editando um arquivo de configuração. Atributos de configuração adicionais são fornecidos pelo catálogo padrão ( [!DNL default.ini]) ou catálogos de materiais específicos. Consulte Catálogos de materiais para obter detalhes.

A pasta de instalação da Renderização de imagem ( *[!DNL install_folder]*) é [!DNL *[!DNL install_root]*/ImageRendering]. No Windows, o padrão *[!DNL install_root]* é `C:\Program Files\Scene7`. Uma pasta diferente pode ser especificada durante a instalação. No Linux, *[!DNL install_root]* deve sempre ser [!DNL /usr/local/scene7]. Podem ser usados links simbólicos.

Todos os caminhos de arquivo fazem distinção entre maiúsculas e minúsculas no UNIX e não fazem distinção entre maiúsculas e minúsculas no Windows.
