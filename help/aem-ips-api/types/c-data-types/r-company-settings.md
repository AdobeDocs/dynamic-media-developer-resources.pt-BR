---
description: Configurações específicas da empresa.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# CompanySettings{#companysettings}

Configurações específicas da empresa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | Determina se as imagens devem ser substituídas na pasta atual com o mesmo nome e extensão de imagem base. |
| `*`keepPublishState`*` | `xsd:boolean` | Especifica se uma imagem de substituição carregada no IPS deve manter a configuração &quot;Pronta para publicação&quot; existente ou se deve ser a especificada pelo upload. |
| `*`defaultSourceProfile`*` | `types:Asset` | Especifica o perfil de cor de origem padrão (Coated FOGRA27 (ISO 126472:2004)) aplicado automaticamente como parte do &quot;Use default Color Behavior&quot; ao adicionar arquivos de imagem CMYK. |
| `*`defaultDisplayProfile`*` | `types:Asset` | Especifica o perfil de cor interna padrão (U.S. Web Coated (SWOP) v2) aplicado automaticamente como parte do &quot;Usar comportamento de cor padrão&quot; ao adicionar arquivos de imagem CMYK. |
| `*`iptcExifMappingXslt`*` | `types:Asset` | A extração de dados de cabeçalho de imagem IPTC e EXIF para o IPS requer uma conversão de nomes de campo internos para nomes de campo definidos pelo usuário para a empresa. Determina uma tabela de tradução XSL (o padrão é &quot;Não extrair nenhum campo IPTC ou EXIF&quot;) para imagens carregadas. |
| `*`xmpMappingXslt`*` | `types:Asset` | A extração XMP dados do cabeçalho da imagem no IPS requer uma conversão de nomes de campo internos em nomes de campo definidos pelo usuário para a empresa. Determina uma tabela de tradução XSL (o padrão é &quot;Não extrair nenhum campo de XMP&quot;) para imagens carregadas. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Quantidade mínima de espaço livre em disco do diretório de imagens antes do envio de um aviso. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina se os emails devem ser enviados antes que os itens colocados na lixeira possam ser excluídos automaticamente. |
| `*`javascriptUploadEnabled`*` | `types:Asset` | Determina se os arquivos JavaScript devem ser carregados. Esse é um risco potencial para a segurança, portanto, use essa opção com cuidado. |

