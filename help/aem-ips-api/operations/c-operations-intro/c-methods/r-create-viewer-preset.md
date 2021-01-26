---
description: Cria uma visualização predefinida que determina o que um usuário pode ver. O visualizador pode ser de qualquer tipo disponível no IPS. A visualização predefinida é aplicada quando os ativos são publicados.
seo-description: Cria uma visualização predefinida que determina o que um usuário pode ver. O visualizador pode ser de qualquer tipo disponível no IPS. A visualização predefinida é aplicada quando os ativos são publicados.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Dynamic Media Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# createViewerPreset{#createviewerpreset}

Cria uma visualização predefinida que determina o que um usuário pode ver. O visualizador pode ser de qualquer tipo disponível no IPS. A visualização predefinida é aplicada quando os ativos são publicados.

Sintaxe

## Tipos de usuário autorizados {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Entrada (createViewerPresetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém as predefinições e os ativos do visualizador. |
| `*`folderHandle`*` | `xsd:string` | Sim | O identificador da pasta que contém os ativos. |
| `*`name`*` | `xsd:string` | Sim | Nome do visualizador. |
| `*`type`*` | `xsd:string` | Sim | Tipo de visualizador. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Não | Uma matriz que contém nomes, valores e alças de imagens às quais você está aplicando predefinições. |

**Saída (createViewerPresetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Sim | Manuseie a predefinição para o visualizador. |

## Exemplos {#section-c88ea63536f3461cbe4677ba53f875dd}

Essa amostra de código cria uma predefinição do player de vídeo. A resposta retorna um identificador para a predefinição.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Resposta**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```

