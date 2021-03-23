---
description: Catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, para o servidor.
seo-description: Catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, para o servidor.
seo-title: Visão geral do catálogo de materiais *
solution: Experience Manager
title: Visão geral do catálogo de materiais *
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Visão geral do catálogo de materiais *{#material-catalog-overview}

Catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, para o servidor.

Cada catálogo de materiais consiste em um *arquivo de atributo de catálogo* necessário e um conjunto de *arquivos de dados de catálogo* opcionais:

* O arquivo de mapa de vinheta, que discrimina vinhetas e modelos e seus metadados associados.
* O arquivo de dados do material, que classifica os materiais e especifica os arquivos e metadados de imagem de textura associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo de mapa de perfil, que discrimina perfis de cores ICC.

Os arquivos de dados do catálogo são associados a catálogos de materiais por referências de arquivo no arquivo de atributo do catálogo. O mesmo arquivo de dados de catálogo pode ser compartilhado por vários catálogos de material.

Os arquivos de atributos do catálogo devem ter um sufixo de arquivo [!DNL .ini] e devem estar localizados na pasta de catálogo *Renderização de imagem* ( [!DNL PlatformServer::ir.catalogRootPath]). Os arquivos de dados do catálogo podem ser localizados na mesma pasta ou em qualquer outra pasta acessível ao Servidor de renderização.

**Atualização de catálogos de materiais**

O servidor monitora continuamente a pasta de catálogo e recarrega automaticamente um catálogo de material, incluindo os arquivos de dados de catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado. Assim, para atualizar catálogos de materiais no servidor, primeiro substitua todos os arquivos de dados do catálogo que precisam ser alterados e depois substitua (ou &quot;toque&quot;) o arquivo de atributos do catálogo para acionar o recarregamento do catálogo.

**Catálogo padrão**

O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de materiais. Se um atributo específico não puder ser encontrado em um catálogo de materiais específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (materiais e perfis ICC). Se um registro de dados específico não puder ser encontrado em um catálogo de materiais específico, o servidor tentará encontrá-lo no catálogo padrão. Isso permite que catálogos de materiais sejam preenchidos de forma esparsa e simplifica o gerenciamento de atributos e dados globais, como modelos compartilhados, macros, fontes etc.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (perfis ICC) quando nenhum catálogo de material específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de Renderização, o arquivo de atributos do catálogo para o catálogo padrão deve ser chamado [!DNL default.ini], sempre deve existir na pasta do catálogo e deve ser totalmente preenchido com todos os atributos necessários, excluindo `attribute::RootId` e as referências para os vários arquivos de dados do catálogo, que são todos opcionais.

**Consulte também**

`PlatformServer::ir.catalogRootPath`
