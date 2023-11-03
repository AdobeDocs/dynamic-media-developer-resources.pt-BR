---
description: Descreve os parâmetros de operação comuns manipulados pela API do Serviço da Web IPS.
solution: Experience Manager
title: Métodos de operações
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Métodos de operações{#operations-methods}

Esta seção descreve os parâmetros de operação comuns manipulados pela API de Serviço da Web IPS.

Para obter uma descrição completa de cada parâmetro de operação, consulte [Parâmetros de operação](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Alças: Sobre {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Manipula objetos IPS de referência retornados por determinadas operações de API. Você também pode passar identificadores como parâmetros para chamadas de operação subsequentes. Os manipuladores são tipos de dados de sequência ( `xsd:string`).

Os manipuladores devem ser usados somente durante uma única sessão do aplicativo. Além disso, você deve tornar os identificadores persistentes, pois seu formato pode mudar entre as versões do IPS. Ao escrever aplicativos interativos, você implementa tempos limite de sessão e descarta todos os identificadores entre sessões, principalmente após uma atualização de IPS. Quando você grava aplicativos não interativos, chame as operações apropriadas para recuperar identificadores toda vez que o aplicativo for executado. As amostras de código Java/Axis2 a seguir mostram uma execução de código incorreta e correta:

**Código de Identificador Incorreto**

Esta amostra de código está incorreta porque contém um valor embutido em código (555) para o identificador da empresa.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Código de alça correto**

Esta amostra de código está correta porque chama `getCompanyInfo` para retornar um identificador válido. Ele não depende de um valor embutido em código. Use este método ou outro equivalente da API IPS para retornar o identificador necessário.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipos de identificador comuns {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

A maioria das operações exige que você defina um contexto de empresa transmitindo um `companyHandle` parâmetro. O identificador da empresa é um ponteiro retornado por determinadas operações, como `getCompanyInfo`, `addCompany`, e `getCompanyMembership`.

**userHandle**

A variável `userHandle` é um parâmetro opcional para operações destinadas a um usuário específico. Por padrão, essas operações se destinam ao usuário que faz a chamada (o usuário cujas credenciais foram passadas para autenticação). No entanto, usuários administradores com as permissões adequadas podem especificar um usuário diferente. Por exemplo, a variável `setPassword` normalmente define a senha do usuário autenticado, mas um administrador pode usar a variável `userHandle` para definir a senha de outro usuário.

Para operações que exigem um contexto de empresa (usando o `companyHandle` ), os usuários autenticados e de destino devem ser membros da empresa especificada. Para operações que não exigem um contexto de empresa, os usuários autenticados e de destino devem ser membros de pelo menos uma empresa comum.

As seguintes operações podem recuperar identificadores de usuário:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Por padrão, as operações que exigem permissões de acesso (leitura, gravação, exclusão) operam no contexto de permissão do usuário que faz a chamada. Certas operações permitem modificar esse contexto com o `accessUserHandle` ou `accessGroupHandle` parâmetro. A variável `accessUserHandle` permite que um administrador personifique outro usuário. A variável `accessGroupHandle` permite que o chamador opere no contexto de um grupo de usuários específico.

**responseFieldArray e excludeFieldArray**

Algumas operações permitem que o chamador restrinja quais campos estão incluídos na resposta. A limitação de campos pode ajudar a reduzir o tempo e a memória necessários para processar a solicitação e reduzir o tamanho dos dados de resposta. O chamador pode solicitar uma lista específica de campos passando um `responseFieldArray` parâmetro ou com uma lista enumerada de campos excluídos por meio do `excludeFieldArray` parâmetro.

Ambos `responseFieldArray` e `excludeFieldArray` especificar campos usando um caminho de nó separado por `/`. Por exemplo, para especificar que `searchAssets` retorna somente o nome, a data da última modificação e os metadados de cada ativo se referem ao seguinte:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Da mesma forma, para retornar todos os campos (exceto permissões):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Observe que os caminhos do nó são relativos à raiz do nó de retorno. Se você especificar um campo de tipo complexo sem qualquer um de seus subelementos (por exemplo, `assetArray/items/imageInfo`), então todos os seus subelementos são incluídos. Se você especificar um ou mais subelementos em um campo de tipo complexo (por exemplo, `assetArray/items/imageInfo/originalPath`), então apenas esses subelementos são incluídos.

Se você não incluir `responseFieldArray` ou `excludeFieldArray` em uma solicitação, todos os campos são retornados.

**Localidade**

A partir do IPS 4.0, a API do IPS oferece suporte à definição do contexto de localidade de uma operação passando o `authHeader` parâmetro de localidade. Se o parâmetro locale não estiver presente, o cabeçalho HTTP `Accept-Language` é usada. Se esse cabeçalho também não estiver presente, o local padrão do servidor IPS será usado.

Certas operações também usam parâmetros de localidade explícitos, que podem ser diferentes do contexto de localidade da operação. Por exemplo, a variável `submitJob` a operação leva um `locale` parâmetro que define a localidade usada para o registro de tarefas e notificação por e-mail.

Os parâmetros de localidade usam o formato `<language_code>[-<country_code>]`

Quando o código de idioma é um código de duas letras em minúsculas especificado pela ISO-639 e o código opcional de país é um código de duas letras em maiúsculas especificado pela ISO-3266. Por exemplo, a cadeia de caracteres local para inglês dos EUA é `en-US`.
