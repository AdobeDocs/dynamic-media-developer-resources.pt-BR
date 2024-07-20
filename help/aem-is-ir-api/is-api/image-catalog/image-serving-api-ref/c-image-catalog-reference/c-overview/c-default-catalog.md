---
description: O catálogo padrão fornece valores padrão para todos os atributos de catálogo para todos os catálogos de imagem.
solution: Experience Manager
title: Catálogo padrão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Catálogo padrão{#default-catalog}

O catálogo padrão fornece valores padrão para todos os atributos de catálogo para todos os catálogos de imagem.

Se um determinado atributo não puder ser encontrado em um catálogo de imagens específico, o servidor usará o valor correspondente do catálogo padrão. Da mesma forma, o catálogo padrão pode ser usado para fornecer padrões para registros de dados de catálogo específicos (imagens, definições de macro, fontes e perfis ICC). Se um registro de dados específico não puder ser encontrado em um catálogo de imagens específico, o servidor tentará encontrá-lo no catálogo padrão. Isso permite que os catálogos de imagem sejam populados de forma esparsa e simplifica o gerenciamento de atributos e dados globais, como modelos compartilhados, macros, fontes e assim por diante.

Além disso, o catálogo padrão fornece todos os atributos e registros de dados (macros, fontes, perfis ICC, regras de pré-processamento de solicitação) quando nenhum catálogo de imagens específico está envolvido em uma operação.

Para o funcionamento correto do [!DNL Platform Server], o arquivo de atributos do catálogo para o catálogo padrão deve ser nomeado como [!DNL default.ini], deve sempre existir na pasta do catálogo e deve ser totalmente preenchido com todos os atributos necessários, excluindo `attribute::RootId` e as referências aos vários arquivos de dados do catálogo, que são todos opcionais.

>[!NOTE]
>
>Todos os arquivos de atributos de catálogo, exceto [!DNL default.ini], devem conter um valor `attribute::RootId` exclusivo. `attribute::RootId` em [!DNL default.ini] deve estar vazio.
