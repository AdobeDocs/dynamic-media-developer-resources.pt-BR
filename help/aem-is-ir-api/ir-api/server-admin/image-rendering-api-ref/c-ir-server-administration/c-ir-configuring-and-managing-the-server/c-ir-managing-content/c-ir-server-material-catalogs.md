---
description: Catálogos de materiais fornecem muitas configurações de Renderização de imagem.
solution: Experience Manager
title: Catálogos de materiais
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Catálogos de materiais{#material-catalogs}

Catálogos de materiais fornecem muitas configurações de Renderização de imagem.

Os catálogos de materiais mapeiam a vinheta e as IDs de material usadas nas solicitações para caminhos de arquivo reais, podem armazenar todos os metadados associados aos materiais e fornecer contêineres para modelos. Eles controlam os perfis ICC e as macros de comando.

Os catálogos de materiais são acessados somente pelo componente Java de Renderização de imagem (co-localizado com o [!DNL Platform Server]). Os arquivos de atributo de catálogo devem ter um sufixo [!DNL .ini] e ser colocados na pasta de catálogo registrada ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). O catálogo de materiais padrão ( [!DNL default.ini]) deve estar sempre presente e deve ser preenchido com todos os atributos para o funcionamento correto do Servidor de imagens.
