---
description: O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo de catálogo principal foi alterado.
solution: Experience Manager
title: Atualização de catálogos de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Atualização de catálogos de imagens{#updating-image-catalogs}

O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo de catálogo principal foi alterado.

Para atualizar catálogos de imagens no servidor, primeiro substitua todos os arquivos de dados de catálogo que precisam ser alterados e, em seguida, substitua (ou &quot;toque&quot; para atualizar a data do arquivo) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

## Atualizações incrementais {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

O carregamento e o processamento de grandes catálogos de imagens podem colocar uma carga substancial no servidor e podem ter um impacto negativo nas operações de servidor ativo. Para minimizar esse impacto, é recomendável implementar um mecanismo de atualização de catálogo incremental, que funciona da seguinte maneira:

Um arquivo de catálogo principal contendo todas as imagens é carregado durante a noite durante horas de tráfego baixo. Se for necessário durante o dia adicionar ou alterar registros no catálogo de imagens, outro arquivo de dados de imagem será criado e conterá apenas os registros novos ou alterados. Este arquivo está registrado como um arquivo de dados de imagem secundário no `attribute::CatalogFile`. O servidor detecta que o arquivo de atributo de catálogo foi alterado e, em seguida, verifica quais arquivos de dados de catálogo foram alterados. Se o arquivo de dados da imagem principal não tiver sido tocado, o servidor carregará ou recarregará somente o arquivo de dados incrementais. Como esse arquivo normalmente é muito menor que o arquivo do catálogo principal, o impacto no servidor é muito menor em comparação com o recarregamento do catálogo principal.

Atualizações incrementais podem reduzir significativamente o impacto no servidor durante tráfego intenso. É recomendável mesclar regularmente o arquivo de dados do catálogo incremental no arquivo de dados do catálogo principal durante horas de tráfego baixo para manter o desempenho ideal do servidor.
