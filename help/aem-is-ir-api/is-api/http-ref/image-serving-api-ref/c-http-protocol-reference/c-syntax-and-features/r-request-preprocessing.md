---
description: O Image Serving fornece um pré-processador de solicitação simples com base nas regras de substituição e correspondência de expressões regulares.
solution: Experience Manager
title: Solicitar pré-processamento
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Solicitar pré-processamento{#request-preprocessing}

O Image Serving fornece um pré-processador de solicitação simples com base nas regras de substituição e correspondência de expressões regulares.

Coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de imagem, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitação podem modificar o caminho e as partes de consulta das solicitações antes de serem processadas pelo analisador do Servidor de Plataforma, incluindo manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos de segurança que normalmente são controlados apenas com atributos de catálogo, como ofuscação de solicitação, marcação de água, bem como limitar o serviço HTTP a endereços IP de cliente específicos.

As regras de pré-processamento de solicitações são adequadas para uma variedade de aplicativos, alguns dos quais são listados abaixo:

* Implemente um mecanismo *caminhos virtuais*, que permite remapear o caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Aplicação seletiva de recursos de segurança, como marcas d&#39;água, filtrados por nome ou caminho de imagem.
* Omitir marcas d&#39;água ou outros recursos de segurança ao acessar o servidor a partir de endereços IP específicos.
* Forçar a aplicação de comandos, como `defaultImage=`, a todas as solicitações ou a solicitações que exibem um padrão específico no caminho do URL ou nas sequências de consulta.
* Não permitindo o uso de comandos com uso intensivo da CPU para impedir o abuso do servidor.
* Permitir que imagens de origem sejam localizadas em servidores HTTP ou FTP enquanto ainda as especifica no caminho da solicitação em vez de com `src=`.
* Controlar configurações de qualidade de imagem (como qualidade JPEG ou nitidez) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na [Referência do conjunto de regras](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consulte também {#see-also}

[Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) do conjunto de regras,  [atributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
