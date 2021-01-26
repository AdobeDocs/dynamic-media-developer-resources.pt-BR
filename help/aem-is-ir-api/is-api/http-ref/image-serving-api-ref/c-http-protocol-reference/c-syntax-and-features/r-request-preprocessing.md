---
description: O Serviço de imagem fornece um pré-processador de solicitação simples com base em regras de substituição e correspondência de expressão regular.
seo-description: O Serviço de imagem fornece um pré-processador de solicitação simples com base em regras de substituição e correspondência de expressão regular.
seo-title: Pré-processamento da solicitação
solution: Experience Manager
title: Pré-processamento da solicitação
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Pré-processamento da solicitação{#request-preprocessing}

O Serviço de imagem fornece um pré-processador de solicitação simples com base em regras de substituição e correspondência de expressão regular.

Coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de imagens, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitações podem modificar as partes de caminho e query das solicitações antes de serem processadas pelo analisador do Servidor de Plataformas, incluindo manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos de segurança que normalmente são controlados apenas com atributos de catálogo, como ofuscação de solicitação, marcação de água, além de limitar o serviço HTTP a endereços IP de cliente específicos.

As regras de pré-processamento de solicitações são adequadas para uma variedade de aplicativos, alguns dos quais estão listados abaixo:

* Implemente um mecanismo de *caminhos virtuais*, que permite o remapeamento do caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Impor seletivamente recursos de segurança, como a marca d&#39;água, filtrados por nome de imagem ou caminho.
* Omitir marcas d&#39;água ou outros recursos de segurança ao acessar o servidor a partir de endereços IP específicos.
* Forçar a aplicação de comandos, como `defaultImage=`, a todas as solicitações ou a solicitações que exibem um padrão específico no caminho do URL ou sequências de caracteres do query.
* Não permitir o uso de comando(s) que consomem muita CPU para impedir o abuso do servidor.
* Permitir que as imagens de origem sejam localizadas em servidores HTTP ou FTP enquanto ainda as especificam no caminho da solicitação em vez de com `src=`.
* Controle as configurações de qualidade de imagem (como qualidade JPEG ou nitidez) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na [Referência do conjunto de regras](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consulte também {#see-also}

[Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) do conjunto de regras,  [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
