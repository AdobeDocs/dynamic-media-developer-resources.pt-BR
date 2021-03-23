---
description: O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.
seo-description: O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.
seo-title: Catálogo padrão
solution: Experience Manager
title: Catálogo padrão
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Catálogo padrão{#default-catalog}

O catálogo padrão fornece valores padrão para todos os atributos do catálogo para todos os catálogos de imagens.

Se um atributo específico não puder ser encontrado em um catálogo de imagem específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (imagens, definições de macro, fontes e perfis ICC). Se um registro de dados específico não puder ser encontrado em um catálogo de imagem específico, o servidor tentará encontrá-lo no catálogo padrão. Isso permite que os catálogos de imagens sejam preenchidos de forma esparsa e simplifica o gerenciamento de atributos e dados globais, como modelos compartilhados, macros, fontes, etc.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (macros, fontes, perfis ICC, regras de pré-processamento de solicitação) quando nenhum catálogo de imagem específico está envolvido em uma operação.

Para o funcionamento correto do Servidor de Plataforma, o arquivo de atributos do catálogo para o catálogo padrão deve ser chamado [!DNL default.ini], sempre deve existir na pasta de catálogo e deve ser totalmente preenchido com todos os atributos necessários, excluindo `attribute::RootId` e as referências para os vários arquivos de dados do catálogo, que são todos opcionais.

>[!NOTE]
>
>Todos os arquivos de atributos do catálogo, exceto [!DNL default.ini], devem conter um valor `attribute::RootId` exclusivo. `attribute::RootId` em  [!DNL default.ini] deve estar vazio.

