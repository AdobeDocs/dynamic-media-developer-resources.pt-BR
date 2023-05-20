---
title: Visão geral do catálogo de materiais
description: Os catálogos de materiais fornecem ao servidor informações sobre vinhetas, materiais e dados de suporte, como perfis ICC.
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

Os catálogos de materiais fornecem ao servidor informações sobre vinhetas, materiais e dados de suporte, como perfis ICC.

Cada catálogo de materiais consiste em um catálogo *arquivo de atributo de catálogo* e um conjunto de *arquivos de dados de catálogo*:

* O arquivo do mapa de vinhetas, que apresenta as vinhetas e os modelos, bem como os respectivos metadados.
* O arquivo de dados de material, que discrimina materiais e especifica os arquivos de imagem de textura e metadados associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo do mapa de perfis, que apresenta os perfis de cores do ICC.

Os arquivos de dados de catálogo são associados a catálogos de materiais por referências de arquivo no arquivo de atributo de catálogo. O mesmo arquivo de dados de catálogo pode ser compartilhado por vários catálogos de material.

Os arquivos de atributo de catálogo devem ter um [!DNL `.ini`] sufixo do arquivo e deve estar na Renderização de imagem *pasta de catálogo* ( [!DNL PlatformServer::ir.catalogRootPath]). Os arquivos de dados do catálogo podem estar na mesma pasta ou em qualquer outra pasta acessível ao Servidor de renderização.

**Atualizando catálogos de material**

O servidor monitora continuamente a pasta do catálogo. Ele recarrega automaticamente um catálogo de materiais — incluindo arquivos de dados de catálogo associados — quando detecta que o arquivo de atributo de catálogo principal foi alterado. Assim, para atualizar catálogos de materiais no servidor, substitua primeiro todos os arquivos de dados de catálogo que precisam ser alterados e substitua (ou &quot;toque&quot;) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

**Catálogo padrão**

O catálogo padrão fornece valores padrão para todos os atributos de catálogo de todos os catálogos de materiais. Se um determinado atributo não puder ser encontrado em um catálogo de materiais específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (materiais e perfis ICC). Se um determinado registro de dados não puder ser encontrado em um catálogo de materiais específico, o servidor tentará encontrá-lo no catálogo padrão. Isso permite que os catálogos de materiais sejam preenchidos de forma esparsa e simplifica o gerenciamento de atributos e dados globais, como modelos, macros e fontes compartilhados.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (perfis ICC) quando nenhum catálogo de materiais específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de renderização, o arquivo de atributos do catálogo para o catálogo padrão deve ser nomeado [!DNL default.ini]. Ele também deve existir sempre na pasta do catálogo e deve ser totalmente preenchido com todos os atributos necessários, excluindo `attribute::RootId` e as referências aos vários arquivos de dados de catálogo, que são opcionais.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
