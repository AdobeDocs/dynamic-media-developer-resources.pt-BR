---
title: Pré-processamento de solicitação
description: A Renderização de imagem fornece um pré-processador de solicitação simples com base na correspondência de expressão regular e regras de substituição.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
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
