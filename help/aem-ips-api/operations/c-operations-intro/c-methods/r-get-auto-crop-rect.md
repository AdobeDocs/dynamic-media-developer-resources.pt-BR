---
description: Retorna uma região cortada para uma imagem com base em sua cor de fundo ou transparência.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# getAutoCropRect{#getautocroprect}

Retorna uma região cortada para uma imagem com base em sua cor de fundo ou transparência.

Sintaxe

## Tipos de usuário autorizados {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Entrada (getAutoCropRectParam)**

>[!NOTE]
>
>Especifique autoColorCropOptions ou autoTransparentCropOptions ao chamar este método.

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com o ativo que deseja trabalhar. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo com o qual você deseja trabalhar. |
| autoColorCropOptions | `types:AutoColorCropOptions` | Não | Calcular retângulo de corte com base na cor. Consulte [Opções deCortarCorAutomática](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | Não | Calcule o retângulo de corte com base na transparência. Consulte [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Saída (getAutoCropRectReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| xOffset | `xsd:int` | Sim | A coordenada inicial de pixels à esquerda da região de corte calculada. |
| Deslocamento | `xsd:int` | Sim | A coordenada de pixel superior inicial da região de corte calculada. |
| largura | `xsd:int` | Sim | Largura da região de corte calculada (em pixels). |
| altura | `xsd:int` | Sim | Altura da região de corte calculada (em pixels). |

## Exemplos {#section-ba65bd66086d491cad1cea535954ee1f}

**Solicitação**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Resposta**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [Opções deCortarCorAutomática](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

