---
description: A Renderização de imagem fornece uma simples solicitação pré-processador com base em regras de substituição e correspondência de expressão regular.
seo-description: A Renderização de imagem fornece uma simples solicitação pré-processador com base em regras de substituição e correspondência de expressão regular.
seo-title: Solicitação pré-processamento *
solution: Experience Manager
title: Solicitação pré-processamento *
topic: Scene7 Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Solicitar pré-processamento *{#request-pre-processing}

A Renderização de imagem fornece uma simples solicitação pré-processador com base em regras de substituição e correspondência de expressão regular.

Coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de materiais, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitação podem modificar o caminho e as partes de query das solicitações antes de serem processadas pelo analisador de Renderização de imagem, incluindo manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos que normalmente são controlados apenas com atributos de catálogo, como definir o tamanho padrão da imagem de resposta ou limitar o serviço HTTP a endereços IP específicos do cliente.

As regras de pré-processamento de solicitações são adequadas para uma variedade de aplicativos, alguns dos quais listados abaixo:

* Implemente um mecanismo de *caminhos virtuais*, que permite o remapeamento do caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Não permitir o uso de comandos com uso intenso da CPU para evitar o abuso do servidor.
* Controle as configurações de qualidade de imagem (como qualidade JPEG ou nitidez) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na Referência do conjunto de regras.

Consulte também Referência do conjunto de regras, atributo::RuleSetFile
