---
description: Crie um novo mapa de imagem ou edite um mapa existente.
seo-description: Crie um novo mapa de imagem ou edite um mapa existente.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Dynamic Media Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# saveImageMap{#saveimagemap}

Crie um novo mapa de imagem ou edite um mapa existente.

Sintaxe

## Tipos de usuário autorizados {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Entrada (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> A alça da empresa com o mapa de imagem que você deseja salvar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador do ativo de imagem ao qual o mapa de imagem pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> A alça do mapa de imagem. Cria um mapa de imagem se NULO. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O nome do mapa de imagem criado ou salvo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Escolha da forma da região. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> região  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Uma lista de pontos delimitada por vírgulas que define a região. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ação  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>O valor <span class="codeph"> href </span> associado ao mapa de imagem, conforme especificado na interface IPS. </p> <p>Para obter o valor <span class="codeph"> href </span>, clique na imagem na interface IPS, copie e cole o URL neste elemento e formate o URL IPS como um URL adequado. Por exemplo, <span class="codeph"> &amp; </span> torna-se <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> posição  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> A ordem na lista de mapas de imagem (o eixo Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Saída (saveImageMapReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Sim | O identificador do mapa de imagem novo ou editado. |

## Exemplos {#section-fdac488b640f427c8aa3d549c5032851}

Essa amostra de código cria um novo mapa de imagem para um ativo. Ele usa um tipo de forma determinado por uma constante de string de forma de região e retorna um identificador para o novo mapa de imagem.

**Solicitação**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Resposta**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```

