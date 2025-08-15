---
description: O Servidor de imagens fornece um pré-processador de solicitação simples com base em regras de correspondência e substituição de expressões regulares.
solution: Experience Manager
title: Pré-processamento de solicitação
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Pré-processamento de solicitação{#request-preprocessing}

O Servidor de imagens fornece um pré-processador de solicitação simples com base em regras de correspondência e substituição de expressões regulares.

Coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de imagens, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitações podem modificar o caminho e as partes de consulta de solicitações antes que elas sejam processadas pelo analisador de [!DNL Platform Server], incluindo manipulação do caminho, adição de comandos, alteração de valores de comando e aplicação de modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos de segurança que normalmente são controlados apenas com atributos de catálogo, como ofuscação de solicitação, marca d&#39;água, bem como limitar o serviço HTTP a endereços IP de clientes específicos.

As regras de pré-processamento de solicitações são adequadas para vários aplicativos, alguns dos quais estão listados abaixo:

* Implemente um mecanismo de *caminhos virtuais*, que permite o remapeamento do caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Aplicação seletiva de recursos de segurança, como marca d&#39;água, filtrados por nome de imagem ou caminho.
* Omissão de marcas d&#39;água ou outros recursos de segurança ao acessar o servidor de endereços IP específicos.
* Forçando a aplicação de comandos, como `defaultImage=`, a todas as solicitações ou solicitações que exibem um padrão específico no caminho de URL ou cadeias de caracteres de consulta.
* Proibir o uso de comando(s) intensivo(s) do CPU para evitar abuso de servidor.
* Permitindo que as imagens de origem sejam localizadas em servidores HTTP ou FTP enquanto ainda as especificam no caminho da solicitação em vez de com `src=`.
* Controle as configurações de qualidade da imagem (como qualidade ou nitidez do JPEG) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na [Referência do Conjunto de Regras](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consulte também {#see-also}

[Referência do Conjunto de Regras](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
