---
description: O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.
seo-description: O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.
seo-title: Catálogo padrão
solution: Experience Manager
title: Catálogo padrão
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catálogo padrão{#default-catalog}

O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.

Se um atributo específico não puder ser encontrado em um catálogo de imagens específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (imagens, definições de macro, fontes e perfis ICC). Se um registro de dados específico não for encontrado em um catálogo de imagens específico, o servidor tentará localizá-lo no catálogo padrão. Isso permite que os catálogos de imagens sejam preenchidos com pouca frequência e simplifica o gerenciamento de atributos e dados globais, como modelos compartilhados, macros, fontes etc.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (macros, fontes, perfis ICC, regras de pré-processamento de solicitação) quando nenhum catálogo de imagem específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de plataforma, o arquivo de atributos do catálogo para o catálogo padrão deve ser nomeado [!DNL default.ini], deve existir sempre na pasta do catálogo e deve ser preenchido completamente com todos os atributos necessários, exceto `attribute::RootId` as referências aos vários arquivos de dados do catálogo, que são todos opcionais.

>[!NOTE]
>
>Todos os arquivos de atributos do catálogo, exceto [!DNL default.ini] devem conter um `attribute::RootId` valor exclusivo. `attribute::RootId` in [!DNL default.ini] deve estar vazio.

