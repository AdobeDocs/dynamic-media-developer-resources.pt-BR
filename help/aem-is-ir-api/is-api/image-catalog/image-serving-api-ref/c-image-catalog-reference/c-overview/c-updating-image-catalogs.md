---
description: O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados do catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.
seo-description: O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados do catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.
seo-title: Atualização de catálogos de imagens
solution: Experience Manager
title: Atualização de catálogos de imagens
topic: Scene7 Image Serving - Image Rendering API
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Atualização de catálogos de imagens{#updating-image-catalogs}

O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados do catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.

Para atualizar catálogos de imagens no servidor, primeiro substitua todos os arquivos de dados do catálogo que precisam ser alterados e depois substitua (ou &quot;toque&quot; para atualizar a data do arquivo) o arquivo de atributos do catálogo para disparar o recarregamento do catálogo.

## Atualizações incrementais {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

O carregamento e o processamento de grandes catálogos de imagens podem colocar uma carga substancial no servidor e podem ter um impacto negativo nas operações de serviço ao vivo. Para minimizar esse impacto, é recomendável implementar um mecanismo de atualização de catálogo incremental, que funciona da seguinte forma:

Um arquivo de catálogo principal que contém todas as imagens é carregado noturna durante horas de tráfego baixas. Se durante o dia for necessário adicionar ou alterar registros no catálogo de imagens, outro arquivo de dados de imagem será criado contendo apenas os registros novos ou alterados. Esse arquivo é registrado como um arquivo de dados de imagem secundário no `attribute::CatalogFile`. O servidor detecta que o arquivo de atributo do catálogo foi alterado e verifica quais arquivos de dados do catálogo foram alterados. Se o arquivo de dados da imagem principal não tiver sido tocado, o servidor carregará ou recarregará apenas o arquivo de dados incremental. Como esse arquivo normalmente é muito menor do que o arquivo do catálogo principal, o impacto no servidor é muito reduzido em comparação ao recarregamento do catálogo principal.

Atualizações incrementais podem reduzir significativamente o impacto no servidor durante o tráfego intenso. É recomendável mesclar regularmente o arquivo de dados de catálogo incremental no arquivo de dados do catálogo principal durante horários de baixo tráfego para manter o desempenho ideal do servidor.
