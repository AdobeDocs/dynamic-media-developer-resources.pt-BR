---
description: Os arquivos de dados de origem da Renderização de Imagem incluem arquivos de vinheta, arquivos de material (imagens para texturas e decalques repetíveis, bem como arquivos de estilo com cobertura de gabinete e janela) e perfis ICC.
solution: Experience Manager
title: Dados de origem
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Dados de origem{#source-data}

Os arquivos de dados de origem da Renderização de Imagem incluem arquivos de vinheta, arquivos de material (imagens para texturas e decalques repetíveis, bem como arquivos de estilo com cobertura de gabinete e janela) e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao componente de código nativo da Renderização de imagem (co-localizado com o Servidor de imagem).

Se um catálogo de materiais estiver envolvido, o arquivo especificado no catálogo de materiais (com `vignette::Path`, `catalog::Path` ou `icc::ProfilePath`) será pesquisado pelo Servidor de Renderização da seguinte maneira:

* Se o caminho for absoluto, ele será usado como está.
* Se o caminho for relativo, ele terá o prefixo `catalog::RootPath` (de um catálogo de materiais nomeado).
* Se o caminho for absoluto, ele será usado; caso contrário, ele terá o prefixo `default::RootPath` (do catálogo padrão).
* Se o caminho for absoluto, ele será usado; caso contrário, o servidor o combina com o caminho especificado em [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Se o caminho agora for absoluto, ele será usado; caso contrário, presume-se que seja relativo a [!DNL *[!DNL install_folder]*].

Se nenhum catálogo de imagem estiver envolvido, o caminho será combinado com `default::RootPath` e processado como acima.

O local físico dos arquivos de dados de origem normalmente é especificado com [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Vários valores podem ser especificados para permitir que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor de Renderização tentará cada caminho na ordem especificada até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
