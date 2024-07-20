---
description: O Serviço Web IPS é suportado por um conjunto de documentos WSDL (Web Services Description Language) que são acessados de qualquer instalação IPS na qual o componente Serviço Web IPS está instalado. Cada versão da API IPS inclui um novo arquivo WSDL que faz referência a um namespace XML de destino com versão. As versões anteriores do namespace WSDL também são compatíveis para permitir compatibilidade com versões anteriores de aplicativos existentes.
solution: Experience Manager
title: Versões WSDL do Serviço Web IPS
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Versões WSDL do Serviço Web IPS{#ips-web-service-wsdl-versions}

O Serviço Web IPS é suportado por um conjunto de documentos WSDL (Web Services Description Language) que são acessados de qualquer instalação IPS na qual o componente Serviço Web IPS está instalado. Cada versão da API IPS inclui um novo arquivo WSDL que faz referência a um namespace XML de destino com versão. As versões anteriores do namespace WSDL também são compatíveis para permitir compatibilidade com versões anteriores de aplicativos existentes.

## Acesso WSDL {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Acesse os WSDLs do Scene7 conforme mostrado abaixo.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

O valor padrão para `<IPS_webapp>` é `scene7`.

**Local do serviço**

A URL do serviço é especificada na seção de serviço do documento WSDL do serviço Web IPS. O URL de serviço geralmente tem o formato:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**URLs de acesso para regiões do Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Localização geográfica </p> </th> 
   <th colname="col2" class="entry"> <p>URL de produção </p> </th> 
   <th colname="col3" class="entry"> <p>URL de preparo (use para desenvolvimento e teste de pré-produção) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>América do Norte </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Oriente Médio e Ásia </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japão/Pacífico Asiático </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## WSDLs compatíveis {#section-ebbba69880f94e9c823f1147974eb404}

Lembre-se, talvez seja necessário modificar seu código se quiser usar recursos na versão mais recente da API do IPS. A API do IPS é compatível com WSDLs para as seguintes versões:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Versão de lançamento da API </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>Namespace da API </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pré-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Os aplicativos existentes que precisam ser modificados para usar os novos recursos devem ser atualizados para a versão mais recente da API e podem precisar fazer alterações no código existente. Consulte o log de alterações para obter detalhes.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Associações**

O Serviço Web da API de IPS oferece suporte somente a uma vinculação de SOAP.

**Transportes com suporte**

A ligação IPS API SOAP é compatível apenas com transporte HTTP. Faça todas as solicitações de SOAP usando o método POST HTTPS.

**Cabeçalho da ação do SOAP**

Para processar uma solicitação, defina o cabeçalho HTTP SOAPAction como o nome da operação solicitada. O atributo nome da operação na seção de vinculação WSDL especifica o nome.

**Formato da mensagem**

O estilo documento/literal é usado para todas as mensagens de entrada e saída com tipos baseados na linguagem de definição do Esquema XML ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) e especificados no arquivo WSDL. Todos os tipos exigem nomes qualificados usando o valor do namespace de destino especificado no arquivo WSDL.

**Solicitar autenticação**

O método preferido para transmitir credenciais de autenticação em solicitações de API é usar o elemento `authHeader` conforme definido no WSDL da API do IPS.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Campos**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> usuário </span> </p> </td> 
   <td colname="col2"> <p> Email de usuário de IPS válido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> senha </span> </p> </td> 
   <td colname="col2"> <p>Senha da conta de usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> localidade </span> </p> </td> 
   <td colname="col2"> <p> Localidade opcional para a solicitação. Consulte <b>Local</b> para obter detalhes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Chamando nome do aplicativo. Esse parâmetro é opcional, mas é recomendável incluí-lo em todas as solicitações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Chamando versão do aplicativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Sinalizador opcional para ativar ou desativar a compactação gzip do XML de resposta. Por padrão, as respostas são compactadas por gzip se o cabeçalho Accept-Encoding do HTTP indicar suporte para gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Parâmetro opcional para substituir o código de status HTTP das respostas a falhas. Por padrão, as respostas de falha retornam o código de status HTTP 500 (Erro interno do servidor). Algumas plataformas clientes, incluindo o Flash Adobe, não conseguem ler o corpo da resposta a menos que um código de status 200 (OK) seja retornado. </p> </td> 
  </tr> 
 </tbody> 
</table>

O elemento `authHeader` sempre é definido no namespace `http://www.scene7.com/IpsApi/xsd`, independentemente da versão da API.

Este é um exemplo de uso do elemento `authHeader` em um cabeçalho SOAP de solicitação:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Outros métodos de autenticação de solicitação**

Se, por algum motivo, seu aplicativo cliente não puder passar o cabeçalho SOAP `authHeader`, as solicitações de API também poderão especificar credenciais usando a autenticação básica de HTTP (conforme especificado no RFC 2617).

Para autenticação básica de HTTP, a seção do cabeçalho HTTP de cada solicitação de POST SOAP deve incluir um cabeçalho no formato:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Onde `base64()` aplica a codificação Base64 padrão, `<IPS_user_email>` é o endereço de email de um usuário de IPS válido e `<password>` é a senha do usuário.

Envie o cabeçalho de Autorização preventivamente com a solicitação inicial. Se nenhuma credencial de autenticação estiver incluída na solicitação, `IpsApiService` não responderá com um código de status de `401 (Unauthorized)`. Em vez disso, um código de status de `500 (Internal Server Error)` é retornado com um corpo de falha SOAP informando que a solicitação não pôde ser autenticada.

Antes do IPS 3.8, a autenticação por meio do cabeçalho SOAP era implementada usando os elementos `AuthUser` e `AuthPassword` no namespace `http://www.scene7.com/IpsApi`. Por exemplo:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Este estilo ainda é suportado para compatibilidade com versões anteriores, mas foi substituído em favor do elemento `authHeader`.

**Solicitar autorização**

Após as credenciais do chamador serem autenticadas, a solicitação é verificada para garantir que o chamador esteja autorizado a executar a operação solicitada. A autorização é baseada na função de usuário do chamador e também pode exigir a verificação da empresa de destino, usuário de destino e outros parâmetros de operação. Além disso, os usuários do Portal de imagens devem pertencer a um Grupo com as permissões necessárias para executar determinadas operações de pastas e ativos. A seção de referência Operações detalha os requisitos de autorização para cada operação.

**Exemplo de solicitação e resposta do SOAP**

O exemplo a seguir mostra uma operação `addCompany` concluída, incluindo cabeçalhos HTTP:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

E a resposta correspondente:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**Falhas de SOAP**

Quando uma operação encontra uma condição de exceção, uma falha do SOAP é retornada como o corpo da mensagem SOAP no lugar da resposta normal. Por exemplo, se um usuário não administrador tentar enviar a solicitação `addCompany` anterior, a seguinte resposta será retornada:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
