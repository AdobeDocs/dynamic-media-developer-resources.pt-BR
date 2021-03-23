---
description: Os catálogos de materiais fornecem muitas configurações de Renderização de Imagem.
seo-description: Os catálogos de materiais fornecem muitas configurações de Renderização de Imagem.
seo-title: Catálogos de materiais
solution: Experience Manager
title: Catálogos de materiais
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Catálogos de materiais{#material-catalogs}

Os catálogos de materiais fornecem muitas configurações de Renderização de Imagem.

Catálogos de materiais mapeiam vinheta e ids de material usadas em solicitações para caminhos de arquivo reais, podem armazenar todos os metadados associados a materiais e fornecer contêineres para modelos. Eles controlam os perfis ICC e as macros de comando.

Os catálogos de materiais são acessados somente pelo componente Java da Renderização de imagem (co-localizado com o Servidor de plataforma). Os arquivos de atributo do catálogo devem ter um sufixo [!DNL .ini] e ser colocados na pasta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). O catálogo de materiais padrão ( [!DNL default.ini]) deve estar sempre presente e deve ser preenchido com todos os atributos para o funcionamento correto do Serviço de imagem.
