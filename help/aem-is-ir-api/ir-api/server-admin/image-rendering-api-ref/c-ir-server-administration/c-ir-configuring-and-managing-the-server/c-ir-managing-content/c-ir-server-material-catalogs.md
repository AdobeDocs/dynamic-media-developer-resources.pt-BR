---
description: Os catálogos de materiais fornecem várias configurações de Renderização de imagem.
seo-description: Os catálogos de materiais fornecem várias configurações de Renderização de imagem.
seo-title: Catálogos de materiais
solution: Experience Manager
title: Catálogos de materiais
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Catálogos de materiais{#material-catalogs}

Os catálogos de materiais fornecem várias configurações de Renderização de imagem.

Os catálogos de materiais mapeiam a vinheta e as IDs de material usadas em solicitações para caminhos de arquivos reais, podem armazenar todos os metadados associados aos materiais e fornecer container para modelos. Eles acompanham perfis ICC e macros de comando.

Os catálogos de materiais são acessados somente pelo componente Java da renderização de imagem (co-localizado com o servidor da plataforma). Os arquivos de atributo do catálogo devem ter um sufixo [!DNL .ini] e ser colocados na pasta de catálogo registrada ([ir.CatalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). O catálogo de materiais padrão ( [!DNL default.ini]) deve estar sempre presente e deve ser preenchido com todos os atributos para o funcionamento correto do Serviço de imagem.
