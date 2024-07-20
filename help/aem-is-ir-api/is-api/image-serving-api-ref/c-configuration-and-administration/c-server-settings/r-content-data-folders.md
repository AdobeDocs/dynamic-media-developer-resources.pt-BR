---
description: Use essas configurações do servidor para pastas de dados de conteúdo.
solution: Experience Manager
title: Pastas de dados de conteúdo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Pastas de dados de conteúdo{#content-data-folders}

Use essas configurações do servidor para pastas de dados de conteúdo.

## IS::RootPath - Pastas raiz de dados de imagem {#section-5c57569514bb4d00b19de31d2e137e3b}

A localização de todos os dados de origem, incluindo imagens, fontes e perfis ICC. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão. Vários valores podem ser especificados para distribuir dados de imagem em vários sistemas de arquivos. O Servidor de imagens tenta os caminhos raiz na ordem especificada, até que o arquivo solicitado seja encontrado.

## PS::staticContent.rootPath - Pastas raiz de dados de conteúdo estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

O local dos dados de fonte de conteúdo estático que devem ser entregues por meio do contexto [!DNL /is/static]. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão.

Vários valores podem ser separados por ponto-e-vírgula para distribuir conteúdo estático entre vários sistemas de arquivos. Normalmente definida com os mesmos valores que `IS::RootPath`.

O [!DNL Platform Server] tenta os caminhos raiz na ordem especificada, até que o arquivo solicitado seja encontrado.

>[!NOTE]
>
>Por padrão, esse campo é intencionalmente definido como um local não existente ([!DNL *[!DNL install_folder]*/static]), desabilitando efetivamente o serviço de conteúdo estático.

## IS::SaveDirectory - Arquivo Salvar Pasta Raiz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

O caminho raiz para `attribute::SavePath` (usado por `req=saveToFile`). O Servidor de imagens deve ter permissões de acesso de criação para a subpasta em que ele cria arquivos de imagem.
