---
description: Configurações específicas da empresa.
solution: Experience Manager
title: Configurações da empresa
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '239'
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
