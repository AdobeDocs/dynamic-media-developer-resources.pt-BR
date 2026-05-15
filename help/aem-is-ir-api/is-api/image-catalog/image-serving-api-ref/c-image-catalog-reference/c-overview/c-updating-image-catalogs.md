---
description: O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo de catálogo principal foi alterado.
solution: Experience Manager
title: Atualização de catálogos de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
TQID: 'https://experienceleague.adobe.com/vnAa-SrnEWsyYW3PuGQT-CjlhGBB9nkQ20hZSKCUuUw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# Atualização de catálogos de imagens{#updating-image-catalogs}

O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de imagens, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo de catálogo principal foi alterado.

Para atualizar catálogos de imagens no servidor, primeiro substitua todos os arquivos de dados de catálogo que precisam ser alterados e, em seguida, substitua (ou &quot;toque&quot; para atualizar a data do arquivo) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

## Atualizações incrementais {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

O carregamento e o processamento de grandes catálogos de imagens podem colocar uma carga substancial no servidor e podem ter um impacto negativo nas operações de servidor ativo. Para minimizar esse impacto, é recomendável implementar um mecanismo de atualização de catálogo incremental, que funciona da seguinte maneira:

Um arquivo de catálogo principal contendo todas as imagens é carregado durante a noite durante horas de tráfego baixo. Se for necessário durante o dia adicionar ou alterar registros no catálogo de imagens, outro arquivo de dados de imagem será criado e conterá apenas os registros novos ou alterados. Este arquivo está registrado como um arquivo de dados de imagem secundário no `attribute::CatalogFile`. O servidor detecta que o arquivo de atributo de catálogo foi alterado e, em seguida, verifica quais arquivos de dados de catálogo foram alterados. Se o arquivo de dados da imagem principal não tiver sido tocado, o servidor carregará ou recarregará somente o arquivo de dados incrementais. Como esse arquivo normalmente é muito menor que o arquivo do catálogo principal, o impacto no servidor é muito menor em comparação com o recarregamento do catálogo principal.

Atualizações incrementais podem reduzir significativamente o impacto no servidor durante tráfego intenso. É recomendável mesclar regularmente o arquivo de dados do catálogo incremental no arquivo de dados do catálogo principal durante horas de tráfego baixo para manter o desempenho ideal do servidor.
