---
description: Os catálogos de materiais fornecem muitas configurações de Renderização de Imagem.
solution: Experience Manager
title: Catálogos de materiais
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Catálogos de materiais{#material-catalogs}

Os catálogos de materiais fornecem muitas configurações de Renderização de Imagem.

Catálogos de materiais mapeiam vinheta e ids de material usadas em solicitações para caminhos de arquivo reais, podem armazenar todos os metadados associados a materiais e fornecer contêineres para modelos. Eles controlam os perfis ICC e as macros de comando.

Os catálogos de materiais são acessados somente pelo componente Java da Renderização de imagem (co-localizado com o Servidor de plataforma). Os arquivos de atributo do catálogo devem ter um sufixo [!DNL .ini] e ser colocados na pasta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). O catálogo de materiais padrão ( [!DNL default.ini]) deve estar sempre presente e deve ser preenchido com todos os atributos para o funcionamento correto do Serviço de imagem.
