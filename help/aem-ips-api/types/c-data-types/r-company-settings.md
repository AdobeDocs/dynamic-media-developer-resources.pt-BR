---
description: Configurações específicas da Empresa.
seo-description: Configurações específicas da Empresa.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

Configurações específicas da Empresa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Determina se as imagens devem ser sobrescritas na pasta atual com o mesmo nome e extensão de imagem base. |
| ` *`keepPublishState`*` | `xsd:boolean` | Especifica se uma imagem de substituição carregada no IPS deve manter a configuração &quot;Pronto para publicar&quot; existente ou se deve ser conforme especificado pelo upload. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Especifica o perfil de cor de origem padrão (Coated FOGRA27 (ISO 126472:2004) automaticamente aplicado como parte do &quot;Usar comportamento de cor padrão&quot; ao adicionar arquivos de imagem CMYK. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Especifica o perfil de cor interno padrão (U.S. Web Coated (SWOP) v2) aplicado automaticamente como parte do &quot;Usar comportamento de cor padrão&quot; ao adicionar arquivos de imagem CMYK. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | A extração de dados de cabeçalho de imagem IPTC e EXIF para IPS requer uma conversão de nomes de campo internos para nomes de campo definidos pelo usuário para a empresa. Determina uma tabela de conversão XSL (o padrão é &quot;Não extrair nenhum campo IPTC ou EXIF&quot;) para imagens carregadas. |
| ` *`xmpMappingXslt`*` | `types:Asset` | A extração dos dados do cabeçalho da imagem XMP para o IPS requer uma conversão de nomes de campo internos para nomes de campo definidos pelo usuário para a empresa. Determina uma tabela de conversão XSL (o padrão é &quot;Não extrair nenhum campo XMP&quot;) para imagens carregadas. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Quantidade mínima de espaço livre em disco do diretório de imagens antes de um aviso ser enviado. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina se é necessário enviar emails antes que os itens colocados no lixo possam ser automaticamente excluídos. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Determina se os arquivos JavaScript devem ser carregados. Este é um risco potencial para a segurança, então use esta opção com cuidado. |

