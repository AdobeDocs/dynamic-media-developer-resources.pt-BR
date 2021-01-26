---
description: Os catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, ao servidor.
seo-description: Os catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, ao servidor.
seo-title: Visão geral do catálogo de materiais *
solution: Experience Manager
title: Visão geral do catálogo de materiais *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Visão geral do catálogo de materiais *{#material-catalog-overview}

Os catálogos de materiais fornecem informações sobre vinhetas, materiais e dados de suporte, como perfis ICC, ao servidor.

Cada catálogo de materiais consiste em um *arquivo de atributo de catálogo* e um conjunto de arquivos de dados de catálogo *opcionais*:

* O arquivo do mapa de vinheta, que apresenta vinhetas e modelos e seus metadados associados.
* O arquivo de dados de material, que categoriza materiais e especifica os arquivos de imagem de textura e os metadados associados.
* O arquivo de definições de macro, que fornece definições para macros de solicitação.
* O arquivo de mapa de perfis, que simboliza perfis de cores ICC.

Os arquivos de dados do catálogo são associados aos catálogos de materiais por referências de arquivo no arquivo de atributos do catálogo. O mesmo arquivo de dados do catálogo pode ser compartilhado por vários catálogos de materiais.

Os arquivos de atributo do catálogo devem ter um sufixo de arquivo [!DNL .ini] e devem estar localizados na pasta de catálogo *Renderização de imagem* ( [!DNL PlatformServer::ir.catalogRootPath]). Os arquivos de dados do catálogo podem ser localizados na mesma pasta ou em qualquer outra pasta acessível ao Servidor de renderização.

**Atualização de catálogos de materiais**

O servidor monitora continuamente a pasta do catálogo e recarrega automaticamente um catálogo de materiais, incluindo os arquivos de dados do catálogo associados, quando detecta que o arquivo de atributo do catálogo principal foi alterado. Assim, para atualizar catálogos de materiais no servidor, substitua primeiro todos os arquivos de dados do catálogo que precisam ser alterados e substitua (ou &quot;toque&quot;) o arquivo de atributos do catálogo para disparar o recarregamento do catálogo.

**Catálogo padrão**

O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de materiais. Se um atributo específico não for encontrado em um catálogo de materiais específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (materiais e perfis ICC). Se um registro de dados específico não for encontrado em um catálogo de materiais específico, o servidor tentará localizá-lo no catálogo padrão. Isso permite que os catálogos de materiais sejam escassamente preenchidos e simplifica o gerenciamento de atributos e dados globais, como modelos compartilhados, macros, fontes etc.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (perfis ICC) quando nenhum catálogo de materiais específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de renderização, o arquivo de atributos do catálogo para o catálogo padrão deve ser chamado de [!DNL default.ini], sempre deve existir na pasta do catálogo e deve ser totalmente preenchido com todos os atributos necessários, excluindo `attribute::RootId` e as referências aos vários arquivos de dados do catálogo, que são todos opcionais.

**Consulte também**

`PlatformServer::ir.catalogRootPath`
