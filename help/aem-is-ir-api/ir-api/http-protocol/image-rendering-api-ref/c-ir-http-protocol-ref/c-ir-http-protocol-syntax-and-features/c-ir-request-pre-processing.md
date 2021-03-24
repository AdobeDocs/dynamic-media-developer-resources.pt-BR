---
description: A Renderização de Imagens fornece um pré-processador de solicitação simples com base nas regras de substituição e correspondência de expressões regulares.
solution: Experience Manager
title: Solicitação de pré-processamento *
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Solicitar pré-processamento *{#request-pre-processing}

A Renderização de Imagens fornece um pré-processador de solicitação simples com base nas regras de substituição e correspondência de expressões regulares.

Coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de materiais, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitação podem modificar o caminho e as partes de consulta das solicitações antes de serem processadas pelo analisador de Renderização de Imagem , incluindo manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos que normalmente são controlados apenas com atributos de catálogo, como definir o tamanho padrão da imagem de resposta ou limitar o serviço HTTP a endereços IP de cliente específicos.

As regras de pré-processamento de solicitações são adequadas para uma variedade de aplicativos, alguns dos quais são listados abaixo:

* Implemente um mecanismo *caminhos virtuais*, que permite remapear o caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Não permitindo o uso de comandos com uso intensivo da CPU para evitar o abuso do servidor.
* Controlar configurações de qualidade de imagem (como qualidade JPEG ou nitidez) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na Referência do conjunto de regras.

Consulte também Referência do conjunto de regras, atributo::RuleSetFile
