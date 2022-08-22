---
title: Visão geral do catálogo de materiais
description: Catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, para o servidor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Visão geral do catálogo de materiais{#material-catalog-overview}

Catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, para o servidor.

Cada catálogo de materiais consiste em um *arquivo de atributo de catálogo* e um conjunto de *arquivos de dados do catálogo*:

* O arquivo de mapa de vinheta, que discrimina vinhetas e modelos e seus metadados associados.
* O arquivo de dados do material, que classifica os materiais e especifica os arquivos e metadados de imagem de textura associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo de mapa de perfil, que discrimina perfis de cores ICC.

Os arquivos de dados do catálogo são associados a catálogos de materiais por referências de arquivo no arquivo de atributo do catálogo. O mesmo arquivo de dados de catálogo pode ser compartilhado por vários catálogos de material.

Os arquivos de atributo do catálogo devem ter um [!DNL `.ini`] sufixo do arquivo e deve estar na Renderização de imagem *pasta de catálogo* ( [!DNL PlatformServer::ir.catalogRootPath]). Os arquivos de dados do catálogo podem estar na mesma pasta ou em qualquer outra pasta acessível ao Servidor de renderização.

**Atualização de catálogos de materiais**

O servidor monitora continuamente a pasta de catálogo. Ele recarrega automaticamente um catálogo de materiais — incluindo arquivos de dados de catálogo associados — quando detecta que o arquivo de atributo do catálogo principal foi alterado. Assim, para atualizar catálogos de materiais no servidor, primeiro substitua todos os arquivos de dados do catálogo que precisam ser alterados e depois substitua (ou &quot;toque&quot;) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

**Catálogo padrão**

O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de materiais. Se um atributo específico não puder ser encontrado em um catálogo de materiais específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (materiais e perfis ICC). Se um registro de dados específico não puder ser encontrado em um catálogo de materiais específico, o servidor tentará encontrá-lo no catálogo padrão. Isso permite que os catálogos de materiais sejam preenchidos de forma esparsa e simplifica o gerenciamento de atributos e dados globais, como modelos, macros e fontes compartilhados.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (perfis ICC) quando nenhum catálogo de material específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de Renderização, o arquivo de atributos do catálogo para o catálogo padrão deve ser nomeado como [!DNL default.ini]. Ele também deve existir sempre na pasta de catálogo e deve ser totalmente preenchido com todos os atributos necessários, exceto `attribute::RootId` e as referências aos vários arquivos de dados do catálogo, que são todos opcionais.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
