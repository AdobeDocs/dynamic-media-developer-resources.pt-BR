---
description: O servidor monitora continuamente a pasta de catálogo e recarrega automaticamente um catálogo de imagem, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.
seo-description: O servidor monitora continuamente a pasta de catálogo e recarrega automaticamente um catálogo de imagem, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.
seo-title: Atualização de catálogos de imagens
solution: Experience Manager
title: Atualização de catálogos de imagens
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---


# Atualização de catálogos de imagens{#updating-image-catalogs}

O servidor monitora continuamente a pasta de catálogo e recarrega automaticamente um catálogo de imagem, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado.

Para atualizar catálogos de imagens no servidor, primeiro substitua todos os arquivos de dados do catálogo que precisam ser alterados e depois substitua (ou &quot;toque&quot; para atualizar a data do arquivo) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

## Atualizações incrementais {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

O carregamento e o processamento de grandes catálogos de imagens podem colocar uma carga substancial no servidor e podem ter um impacto negativo nas operações de fornecimento ao vivo. Para minimizar esse impacto, é recomendável implementar um mecanismo de atualização de catálogo incremental, que funciona da seguinte maneira:

Um arquivo de catálogo principal contendo todas as imagens é carregado durante as horas de tráfego baixo. Se for necessário durante o dia adicionar ou alterar registros no catálogo de imagens, outro arquivo de dados de imagem será criado contendo apenas os registros novos ou alterados. Esse arquivo é registrado como um arquivo de dados de imagem secundário em `attribute::CatalogFile`. O servidor detecta que o arquivo de atributo do catálogo foi alterado e verifica quais arquivos de dados do catálogo foram alterados. Se o arquivo de dados da imagem principal não tiver sido tocado, o servidor carregará ou recarregará somente o arquivo de dados incremental. Como esse arquivo geralmente é muito menor do que o arquivo do catálogo principal, o impacto no servidor é muito reduzido, em comparação com o recarregamento do catálogo principal.

As atualizações incrementais podem reduzir bastante o impacto no servidor durante o tráfego intenso. É recomendável mesclar regularmente o arquivo de dados de catálogo incremental no arquivo de dados do catálogo principal durante horas de tráfego baixo para manter o desempenho ideal do servidor.
