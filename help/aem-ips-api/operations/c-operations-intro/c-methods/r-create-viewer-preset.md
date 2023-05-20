---
description: Cria uma exibição predefinida que determina o que um usuário pode ver. O visualizador pode ser de qualquer tipo disponível no IPS. A exibição predefinida é aplicada quando os ativos são publicados.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# createViewerPreset{#createviewerpreset}

Cria uma exibição predefinida que determina o que um usuário pode ver. O visualizador pode ser de qualquer tipo disponível no IPS. A exibição predefinida é aplicada quando os ativos são publicados.

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém as predefinições e os ativos do visualizador. |
| folderHandle | `xsd:string` | Sim | O identificador da pasta que contém os ativos. |
| name | `xsd:string` | Sim | Nome do visualizador. |
| type | `xsd:string` | Sim | Tipo de visualizador. |
| configSettingArray | `types:ConfigSettingArray` | Não | Uma matriz que contém nomes, valores e identificadores de imagens às quais você está aplicando predefinições. |

**Saída (createViewerPresetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Sim | Identificador da predefinição para o visualizador. |

## Exemplos {#section-c88ea63536f3461cbe4677ba53f875dd}

Este exemplo de código cria uma predefinição do reprodutor de vídeo. A resposta retorna um identificador para a predefinição.

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
