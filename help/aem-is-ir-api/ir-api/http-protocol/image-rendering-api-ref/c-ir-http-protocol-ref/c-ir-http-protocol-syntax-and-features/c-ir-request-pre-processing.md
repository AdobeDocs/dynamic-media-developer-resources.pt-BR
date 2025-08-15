---
title: Pré-processamento de solicitação
description: A Renderização de imagem fornece um pré-processador de solicitação simples com base na correspondência de expressão regular e regras de substituição.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Pré-processamento de solicitação{#request-pre-processing}

A Renderização de imagem fornece um pré-processador de solicitação simples com base na correspondência de expressão regular e regras de substituição.

As coleções de regras (conjuntos de regras) podem ser anexadas a cada catálogo de materiais, incluindo o catálogo padrão. As regras são especificadas com arquivos formatados em XML.

As regras de pré-processamento de solicitações podem modificar o caminho e as partes de consulta de solicitações antes que sejam processadas pelo analisador de Renderização de imagem. Este preceito inclui manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos que normalmente são controlados apenas com atributos de catálogo, como definir o tamanho padrão da imagem de resposta ou limitar o serviço HTTP a endereços IP de clientes específicos.

As regras de pré-processamento de solicitações são adequadas para vários aplicativos, alguns dos quais estão listados abaixo:

* Implemente um mecanismo de *caminhos virtuais*, que permite o remapeamento do caminho da solicitação para caminhos de arquivo, FTP e HTTP.
* Proibição do uso de comandos com uso intensivo do CPU para impedir o abuso do servidor.
* Controle as configurações de qualidade da imagem (como qualidade ou nitidez do JPEG) dependendo do caminho da solicitação ou do nome da imagem.

Informações detalhadas sobre como criar, usar e gerenciar conjuntos de regras podem ser encontradas na Referência do conjunto de regras.

Consulte também Referência do conjunto de regras, atributo::RuleSetFile
