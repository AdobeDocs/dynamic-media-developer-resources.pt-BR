---
description: Descreve os parâmetros de operação comuns manipulados pela API do Serviço Web IPS.
solution: Experience Manager
title: Métodos de operações
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# Métodos de operações{#operations-methods}

Esta seção descreve os parâmetros de operação comuns manipulados pela API do Serviço Web IPS.

Para obter uma descrição completa de cada parâmetro de operação, consulte [Parâmetros de operação](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Identificadores: Sobre {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Trata objetos IPS de referência retornados por determinadas operações de API. Você também pode enviar identificadores como parâmetros para chamadas de operação subsequentes. Identificadores são tipos de dados de string ( `xsd:string`).

Os identificadores destinam-se a ser utilizados apenas durante uma sessão de aplicação única. Além disso, você deve tornar os identificadores persistentes, pois seu formato pode mudar entre as versões do IPS. Ao gravar aplicativos interativos, você implementa tempos limite de sessão e descarta todos os identificadores entre sessões, especialmente após uma atualização do IPS. Ao gravar aplicativos não interativos, chame as operações apropriadas para recuperar identificadores sempre que o aplicativo for executado. As amostras de código Java/Axis2 a seguir mostram a execução incorreta e correta do código:

**Código de Identificador Incorreto**

Esta amostra de código está incorreta porque contém um valor codificado (555) para o identificador da empresa.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código correto de manipulador**

Esta amostra de código está correta porque chama `getCompanyInfo` para retornar um identificador válido. Ele não depende de um valor codificado. Use esse método ou outro equivalente de API IPS para retornar o identificador necessário.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipos de Identificador Comuns {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

A maioria das operações exige que você defina um contexto de empresa transmitindo um `companyHandle` parâmetro. O identificador da empresa é um ponteiro retornado por determinadas operações, como `getCompanyInfo`, `addCompany`e `getCompanyMembership`.

**userHandle**

O `userHandle` é um parâmetro opcional para operações que direcionam um usuário específico. Por padrão, essas operações têm como alvo o usuário que faz a chamada (o usuário cujas credenciais são passadas para autenticação). No entanto, os usuários administradores com as permissões apropriadas podem especificar um usuário diferente. Por exemplo, a variável `setPassword` normalmente define a senha do usuário autenticado, mas um administrador pode usar o `userHandle` para definir a senha de um usuário diferente.

Para operações que exigem um contexto de empresa (usando a variável `companyHandle` ), os usuários autenticados e de destino devem ser membros da empresa especificada. Para operações que não exigem um contexto de empresa, os usuários autenticados e de destino devem ser membros de pelo menos uma empresa comum.

As seguintes operações podem recuperar identificadores de usuário:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Por padrão, as operações que exigem permissões de acesso (ler, gravar, excluir) operam no contexto de permissão do usuário chamador. Certas operações permitem modificar esse contexto com a variável `accessUserHandle` ou `accessGroupHandle` parâmetro. O `accessUserHandle` permite que um administrador represente outro usuário. O `accessGroupHandle` permite que o chamador funcione no contexto de um grupo de usuários específico.

**responseFieldArray e excludeFieldArray**

Algumas operações permitem que o chamador restrinja quais campos estão incluídos na resposta. Limitar campos pode ajudar a reduzir o tempo e a memória necessários para processar a solicitação e reduzir o tamanho dos dados de resposta. O chamador pode solicitar uma lista específica de campos transmitindo um `responseFieldArray` ou com uma lista enumerada de campos excluídos por meio do `excludeFieldArray` parâmetro.

Ambos `responseFieldArray` e `excludeFieldArray` especifique campos usando um caminho de nó separado por `/`. Por exemplo, para especificar que `searchAssets` retorna somente o nome, a data da última modificação e os metadados de cada ativo referentes ao seguinte:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Da mesma forma, para retornar todos os campos (exceto por permissões):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Observe que os caminhos do nó são relativos à raiz do nó de retorno. Se você especificar um campo de tipo complexo sem qualquer um de seus subelementos (por exemplo, `assetArray/items/imageInfo`), todos os seus subelementos são incluídos. Se você especificar um ou mais subelementos em um campo de tipo complexo (por exemplo, `assetArray/items/imageInfo/originalPath`), então apenas esses subelementos são incluídos.

Se você não incluir `responseFieldArray` ou `excludeFieldArray` em uma solicitação, todos os campos são retornados.

**Localidade**

Desde o IPS 4.0, a API do IPS suporta a configuração do contexto de localidade de uma operação ao passar o `authHeader` parâmetro de localidade. Se o parâmetro de localidade não estiver presente, o cabeçalho HTTP `Accept-Language` é usada. Se esse cabeçalho também não estiver presente, a localidade padrão do servidor IPS será usada.

Algumas operações também utilizam parâmetros de localidade explícitos, que podem ser diferentes do contexto de localidade da operação. Por exemplo, a variável `submitJob` a operação `locale` que define o local usado para registro de tarefas e notificação por email.

Os parâmetros de localidade usam o formato `<language_code>[-<country_code>]`

Quando o código linguístico for um código em minúsculas, com duas letras, especificado pela norma ISO-639, e o código opcional do país for um código de duas letras maiúsculas, especificado pela norma ISO-3266. Por exemplo, a sequência de caracteres de localidade para inglês americano é `en-US`.
