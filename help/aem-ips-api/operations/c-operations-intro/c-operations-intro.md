---
description: Descreve os parâmetros de operação comuns manipulados pela API do Serviço Web IPS.
solution: Experience Manager
title: Métodos de operações
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---


# Métodos de operações{#operations-methods}

Esta seção descreve os parâmetros de operação comuns manipulados pela API do Serviço Web IPS.

Para obter uma descrição completa de cada parâmetro de operação, consulte [Parâmetros de operação](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Identificadores: Sobre {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Trata objetos IPS de referência retornados por determinadas operações de API. Você também pode passar identificadores como parâmetros para chamadas de operação subsequentes. Identificadores são tipos de dados de string ( `xsd:string`).

Os identificadores são destinados ao uso apenas durante uma única sessão de aplicativo. Além disso, você deve tornar os identificadores persistentes, pois seu formato pode mudar entre as versões do IPS. Ao gravar aplicativos interativos, você implementa tempos limite de sessão e descarta todas as alças entre sessões, principalmente após uma atualização de IPS. Ao gravar aplicativos não interativos, chame as operações apropriadas para recuperar alças sempre que o aplicativo for executado. As seguintes amostras de código Java/Axis2 mostram execução de código incorreta e correta:

**Código de alça incorreto**

Esta amostra de código está incorreta porque contém um valor codificado (555) para a alça de empresa.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código de alça correto**

Esta amostra de código está correta porque chama `getCompanyInfo` para retornar um identificador válido. Ele não depende de um valor codificado. Use esse método ou outro equivalente de API IPS para retornar o identificador necessário.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipos de Identificadores Comuns {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

A maioria das operações exige que você defina um contexto de empresa transmitindo um parâmetro `companyHandle`. O identificador de empresa é um ponteiro retornado por determinadas operações, como `getCompanyInfo`, `addCompany` e `getCompanyMembership`.

**userHandle**

O parâmetro `userHandle` é um parâmetro opcional para operações que público alvo um usuário específico. Por padrão, essas operações públicos alvos o usuário chamador (o usuário cujas credenciais são enviadas para autenticação). No entanto, os usuários administradores com as permissões apropriadas podem especificar um usuário diferente. Por exemplo, a operação `setPassword` normalmente define a senha do usuário autenticado, mas um administrador pode usar o parâmetro `userHandle` para definir a senha para um usuário diferente.

Para operações que exigem um contexto de empresa (usando o parâmetro `companyHandle`), os usuários autenticados e públicos alvos devem ser membros da empresa especificada. Para operações que não exigem um contexto de empresa, os usuários autenticados e públicos alvos devem ser membros de pelo menos uma empresa comum.

As seguintes operações podem recuperar os identificadores do usuário:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Por padrão, as operações que exigem permissões de acesso (ler, gravar, excluir) operam no contexto de permissão do usuário chamador. Algumas operações permitem modificar esse contexto com o parâmetro `accessUserHandle` ou `accessGroupHandle`. O parâmetro `accessUserHandle` permite que um administrador represente outro usuário. O parâmetro `accessGroupHandle` permite que o chamador funcione no contexto de um grupo de usuários específico.

**responseFieldArray e excludeFieldArray**

Algumas operações permitem que o chamador restrinja quais campos estão incluídos na resposta. A limitação de campos pode ajudar a reduzir o tempo e a memória necessários para processar a solicitação e reduzir o tamanho dos dados de resposta. O chamador pode solicitar uma lista específica de campos transmitindo um parâmetro `responseFieldArray` ou com uma lista enumerada de campos excluídos por meio do parâmetro `excludeFieldArray`.

Ambos `responseFieldArray` e `excludeFieldArray` especificam campos usando um caminho de nó separado por `/`. Por exemplo, para especificar que `searchAssets` retorne somente o nome, a data da última modificação e os metadados de cada ativo, consulte o seguinte:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Da mesma forma, para retornar todos os campos (exceto as permissões):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Observe que os caminhos do nó são relativos à raiz do nó de retorno. Se você especificar um campo de tipo complexo sem qualquer um de seus subelementos (por exemplo, `assetArray/items/imageInfo`), todos os seus subelementos serão incluídos. Se você especificar um ou mais subelementos em um campo de tipo complexo (por exemplo, `assetArray/items/imageInfo/originalPath`), somente esses subelementos serão incluídos.

Se você não incluir `responseFieldArray` ou `excludeFieldArray` em uma solicitação, todos os campos serão retornados.

**Localidade**

Desde o IPS 4.0, a API IPS oferece suporte para a definição do contexto de localidade de uma operação, passando pelo parâmetro de localidade `authHeader`. Se o parâmetro de localidade não estiver presente, o cabeçalho HTTP `Accept-Language` será usado. Se esse cabeçalho também não estiver presente, a localidade padrão do servidor IPS será usada.

Algumas operações também utilizam parâmetros de localidade explícitos, que podem ser diferentes do contexto de localidade da operação. Por exemplo, a operação `submitJob` utiliza um parâmetro `locale` que define a localidade usada para registro de tarefas e notificação por email.

Os parâmetros locais usam o formato `<language_code>[-<country_code>]`

Quando o código linguístico for um código em minúsculas, de duas letras especificado pela norma ISO-639 e o código opcional do país for um código em maiúsculas e de duas letras especificado pela norma ISO-3266. Por exemplo, a string de localidade para inglês dos EUA é `en-US`.
