---
description: Use essas configurações do servidor para pastas de dados de conteúdo.
seo-description: Use essas configurações do servidor para pastas de dados de conteúdo.
seo-title: Pastas de dados de conteúdo
solution: Experience Manager
title: Pastas de dados de conteúdo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Pastas de dados de conteúdo{#content-data-folders}

Use essas configurações do servidor para pastas de dados de conteúdo.

## IS::RootPath - Pastas raiz de dados de imagem {#section-5c57569514bb4d00b19de31d2e137e3b}

O local de todos os dados de origem, incluindo imagens, fontes e perfis ICC. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão. Vários valores podem ser especificados para distribuir dados de imagem em vários sistemas de arquivos. O Servidor de Imagens tentará os caminhos raiz na ordem especificada até que o arquivo solicitado seja encontrado.

## PS::staticContent.rootPath - Pastas raiz de dados de conteúdo estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

A localização dos dados da fonte de conteúdo estático que devem ser entregues pelo contexto [!DNL /is/static]. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto-e-vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão.

Vários valores podem ser especificados separados por ponto-e-vírgula para distribuir conteúdo estático em vários sistemas de arquivos. Normalmente definido para os mesmos valores de `IS::RootPath`.

O Servidor de plataforma tenta os caminhos raiz na ordem especificada até que o arquivo solicitado seja encontrado.

>[!NOTE]
>
>Por padrão, esse campo é definido intencionalmente para um local não existente ( [!DNL *[!DNL install_folder]*/static]), desativando efetivamente o serviço de conteúdo estático.

## IS::SaveDirectory - Arquivo Salvar Pasta Raiz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

O caminho raiz para `attribute::SavePath` (usado por `req=saveToFile`). O Servidor de imagens deve ter permissões de acesso de criação para a subpasta na qual criará arquivos de imagem.
