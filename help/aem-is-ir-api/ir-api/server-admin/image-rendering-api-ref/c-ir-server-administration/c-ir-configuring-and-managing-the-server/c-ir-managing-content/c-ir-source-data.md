---
description: Os arquivos de dados de origem da Renderização de imagem incluem arquivos de vinheta, arquivos de material (imagens para texturas e decalques repetíveis, bem como arquivos de estilo de cobertura de gabinete e janela) e perfis ICC.
solution: Experience Manager
title: Dados de origem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Dados de origem{#source-data}

Os arquivos de dados de origem da Renderização de imagem incluem arquivos de vinheta, arquivos de material (imagens para texturas e decalques repetíveis, bem como arquivos de estilo de cobertura de gabinete e janela) e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao componente de código nativo da Renderização de imagem (co-localizado com o Servidor de imagens).

Se um catálogo de materiais estiver envolvido, o arquivo especificado no catálogo de materiais (com `vignette::Path`, `catalog::Path`ou `icc::ProfilePath`) é pesquisado pelo Servidor de renderização da seguinte maneira:

* Se o caminho for absoluto, será usado como está.
* Se o caminho for relativo, ele receberá o prefixo `catalog::RootPath` (de um catálogo de materiais nomeado).
* Se o caminho for absoluto, será usado; caso contrário, terá o prefixo `default::RootPath` (do catálogo padrão).
* Se o caminho for absoluto, ele será usado; caso contrário, o servidor o combinará com o caminho especificado em [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Se o caminho for agora absoluto, ele será usado; caso contrário, será considerado relativo a [!DNL  *[!DNL install_folder]*].

Se nenhum catálogo de imagens estiver envolvido, o caminho será combinado com `default::RootPath` e, em seguida, processado como acima.

O local físico dos arquivos de dados de origem geralmente é especificado com [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Vários valores podem ser especificados para permitir que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O servidor de renderização tentará cada caminho na ordem especificada até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
