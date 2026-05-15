---
description: Configurações específicas da empresa.
solution: Experience Manager
title: Configurações da empresa
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 0%

---

# [!DNL CompanySettings]{#companysettings}

Configurações específicas da empresa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| overwriteMode | `xsd:string` | Determina se as imagens da pasta atual devem ser substituídas pelo mesmo nome e extensão da imagem base. |
| keepPublishState | `xsd:boolean` | Especifica se uma imagem de substituição carregada no IPS deve manter a configuração existente &quot;Pronta para publicação&quot; ou se deve ser conforme especificado pelo upload. |
| defaultSourceProfile | `types:Asset` | Especifica o perfil de cor de origem padrão (FOGRA27 revestido (ISO 126472:2004)) aplicado automaticamente como parte do comando &quot;Usar comportamento de cor padrão&quot; ao adicionar arquivos de imagem CMYK. |
| defaultDisplayProfile | `types:Asset` | Especifica o perfil de cor interno padrão (SWOP (U.S. Web Coated) v2) aplicado automaticamente como parte do &quot;Usar comportamento de cor padrão&quot; ao adicionar arquivos de imagem CMYK. |
| iptcExifMappingXslt | `types:Asset` | A extração de dados do cabeçalho de imagem do IPTC e EXIF para o IPS requer uma conversão de nomes de campos internos para nomes de campos definidos pelo usuário para a empresa. Determina uma tabela de tradução XSL (o padrão é &quot;Não extrair campos IPTC ou EXIF&quot;) para imagens carregadas. |
| xmpMappingXslt | `types:Asset` | A extração de dados do cabeçalho de imagem do XMP para o IPS requer uma conversão de nomes de campos internos para nomes de campos definidos pelo usuário para a empresa. Determina uma tabela de tradução XSL (o padrão é &quot;Não extrair campos do XMP&quot;) para imagens carregadas. |
| diskSpaceWarningMin | `xsd:int` | Quantidade mínima de espaço livre em disco do diretório de imagens antes do envio de um aviso. |
| emailTrashCleanupWarning | `xsd:boolean` | Determina se os emails devem ser enviados antes que os itens da lixeira sejam excluídos automaticamente. |
| javascriptUploadEnabled | `types:Asset` | Determina se os arquivos do JavaScript devem ser carregados. Essa opção é um risco de segurança em potencial, portanto, use com cuidado. |
