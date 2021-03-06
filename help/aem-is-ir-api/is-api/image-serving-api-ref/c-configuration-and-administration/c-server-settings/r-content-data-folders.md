---
description: Use essas configurações do servidor para pastas de dados de conteúdo.
solution: Experience Manager
title: Pastas de dados de conteúdo
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Pastas de dados de conteúdo{#content-data-folders}

Use essas configurações do servidor para pastas de dados de conteúdo.

## IS::RootPath - Pastas raiz de dados de imagem {#section-5c57569514bb4d00b19de31d2e137e3b}

O local de todos os dados de origem, incluindo imagens, fontes e perfis ICC. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto e vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão. Vários valores podem ser especificados para distribuir dados de imagem em vários sistemas de arquivos. O Servidor de Imagens tentará os caminhos raiz na ordem especificada até que o arquivo solicitado seja encontrado.

## PS::staticContent.rootPath - Pastas raiz de dados de conteúdo estático {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

O local dos dados da fonte de conteúdo estático que deve ser entregue por meio do contexto [!DNL /is/static]. Pode ser um ou mais caminhos de arquivo absolutos ou caminhos relativos a *[!DNL install_folder]*, separados por ponto e vírgula. Se estiver vazio, *[!DNL install_folder]* será a raiz padrão.

Vários valores podem ser especificados-separados por ponto e vírgula para distribuir conteúdo estático em vários sistemas de arquivos. Normalmente, é definido como os mesmos valores de `IS::RootPath`.

O Servidor de Plataforma tenta os caminhos raiz na ordem especificada até que o arquivo solicitado seja encontrado.

>[!NOTE]
>
>Por padrão, esse campo é definido intencionalmente para um local não existente ( [!DNL *[!DNL install_folder]*/static]), desativando efetivamente o serviço de conteúdo estático.

## IS::SaveDirectory - Arquivo Salvar pasta raiz {#section-1c517f8d49ce4cb8b9013e520bf309c9}

O caminho raiz de `attribute::SavePath` (usado por `req=saveToFile`). O Servidor de Imagens deve ter permissões de acesso de criação para a subpasta em que criará arquivos de imagem.
