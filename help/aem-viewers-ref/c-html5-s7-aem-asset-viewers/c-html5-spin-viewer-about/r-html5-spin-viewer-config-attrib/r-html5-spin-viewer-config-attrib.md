---
description: Documentação de atributos de configuração para o visualizador de rotação.
seo-description: Documentação de atributos de configuração para o visualizador de rotação.
seo-title: Referência de comando - Atributos de configuração
solution: Experience Manager
title: Referência de comando - Atributos de configuração
topic: Dynamic media
uuid: ba60da44-d30d-459f-b3d8-5cf3ea4bcbdb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o visualizador de rotação.

Qualquer comando de configuração pode ser definido em URL ou usando `setParam()`, ou `setParams()`, ou ambos, métodos de API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o prefixo nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método `setContainerId()` API. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, `zoomstep` o comando é documentado da seguinte maneira:

`[SpinView.|<containerId>_spinView].zoomstep`

o que significa que você pode usar esse comando como:

* `zoomstep` (sintaxe curta)
* `SpinView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_spinView.zoomstep` (qualificado com a ID do componente, presumindo que `cont` seja a ID do elemento do container)

Consulte também Referência de [comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
