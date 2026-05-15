---
description: O catálogo padrão fornece valores padrão para todos os atributos de catálogo para todos os catálogos de imagem.
solution: Experience Manager
title: Catálogo padrão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
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
