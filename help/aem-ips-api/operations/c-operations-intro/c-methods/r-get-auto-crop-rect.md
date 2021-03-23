---
description: Retorna uma região cortada para uma imagem com base em sua cor de fundo ou transparência.
seo-description: Retorna uma região cortada para uma imagem com base em sua cor de fundo ou transparência.
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '174'
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
>Especifique `*`autoColorCropOptions`*` ou `*`autoTransparentCropOptions`*` ao chamar este método.

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o ativo que deseja trabalhar. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo com o qual você deseja trabalhar. |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | Não | Calcular retângulo de corte com base na cor. Consulte [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | Não | Calcule o retângulo de corte com base na transparência. Consulte [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Saída (getAutoCropRectReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | Sim | A coordenada inicial de pixels à esquerda da região de corte calculada. |
| `*`Deslocamento`*` | `xsd:int` | Sim | A coordenada de pixel superior inicial da região de corte calculada. |
| `*`width`*` | `xsd:int` | Sim | Largura da região de corte calculada (em pixels). |
| `*`altura`*` | `xsd:int` | Sim | Altura da região de corte calculada (em pixels). |

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

