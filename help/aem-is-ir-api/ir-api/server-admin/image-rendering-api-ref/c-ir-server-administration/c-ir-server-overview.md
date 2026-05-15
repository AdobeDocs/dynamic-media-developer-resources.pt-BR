---
description: Esta documentação explica como administrar o servidor de Renderização de imagem do Dynamic Media.
solution: Experience Manager
title: Visão geral da administração do servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# Visão geral da administração do servidor{#server-administration-overview}

Esta documentação explica como administrar o servidor de Renderização de imagem do Dynamic Media.

A Renderização de imagem consiste em dois componentes principais:

* Um pacote Java é implantado com o Servidor de Imagens [!DNL Platform Server] e gerencia a conexão do cliente, o armazenamento em cache e os catálogos de material.
* Um módulo de código nativo é implantado como uma biblioteca de extensões para o Servidor de imagens e implementa as funcionalidades principais de renderização de imagem.

Ambos os componentes são chamados coletivamente de *Servidor de Renderização*.

A Renderização de imagem compartilha vários recursos do servidor com o Servidor de imagens, e todas as opções são configuradas ao editar um arquivo de configuração. Atributos de configuração adicionais são fornecidos pelo catálogo padrão ( [!DNL default.ini]) ou por catálogos de materiais específicos. Consulte Catálogos de materiais para obter detalhes.

A pasta de instalação da Renderização de Imagem ( *[!DNL install_folder]*) é [!DNL *[!DNL install_root]*/ImageRendering]. No Windows, o padrão *[!DNL install_root]* é `C:\Program Files\Scene7`. Uma pasta diferente pode ser especificada durante a instalação. No Linux, *[!DNL install_root]* sempre deve ser [!DNL /usr/local/scene7]. É possível usar links simbólicos.

Todos os caminhos de arquivos fazem distinção entre maiúsculas e minúsculas no UNIX e no Windows.
