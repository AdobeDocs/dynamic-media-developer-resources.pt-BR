---
title: Fazer upload de ativos por meio de POSTs HTTP no Servlet UploadFile
description: O carregamento de ativos no  [!DNL Dynamic Media] Classic envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar todas as atividades de log associadas aos arquivos carregados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Fazer upload de ativos por meio de POSTs HTTP no Servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

O upload de ativos no Dynamic Media Classic envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar todas as atividades de log associadas aos arquivos carregados.

Use o seguinte URL para acessar o Servlet UploadFile:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

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
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Oriente Médio e Ásia </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japão/Pacífico Asiático </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Fluxo de trabalho do trabalho de upload {#section-873625b9512f477c992f5cdd77267094}

O trabalho de carregamento consiste em um ou mais POSTs HTTP que usam um `jobHandle` comum para correlacionar o processamento no mesmo trabalho. Cada solicitação é codificada em `multipart/form-data` e consiste nas seguintes partes de formulário:

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

|  Parte de formulário HTTP POST  |  Descrição  |
|---|---|
| `auth`  |   Obrigatório. Um documento de cabeçalho de autenticação XML que especifica informações de autenticação e do cliente. Consulte **Solicitar autenticação** em [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Opcional. Você pode incluir um ou mais arquivos para fazer upload com cada solicitação POST. Cada parte do arquivo pode incluir um parâmetro de nome de arquivo no cabeçalho Content-Disposition usado como nome de arquivo de destino no IPS se nenhum parâmetro `uploadPostParams/fileName` for especificado. |

|  Parte de formulário HTTP POST   |  nome do elemento uploadPostParams   |  Tipo   |  Descrição   |
|---|---|---|---|
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento)   |   `companyHandle`  |  `xsd:string`  | Obrigatório. Processe a empresa para a qual o arquivo está sendo carregado.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `jobName`  |  `xsd:string`  | `jobName` ou `jobHandle` é obrigatório. Nome do trabalho de upload.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `jobHandle`  |  `xsd:string`  | `jobName` ou `jobHandle` é obrigatório. O processamento de um trabalho de upload foi iniciado em uma solicitação anterior.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `locale`  |  `xsd:string`  | Opcional. Idioma e código do país para localização.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `description`  |  `xsd:string`  | Opcional. Descrição da tarefa.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `destFolder`  |  `xsd:string`  | Opcional. Caminho da pasta de destino para prefixar para uma propriedade de nome de arquivo, especialmente para navegadores e outros clientes que podem não suportar caminhos completos em um nome de arquivo.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `fileName`  |  `xsd:string`  | Opcional. Nome do arquivo de destino. Substitui a propriedade do nome de arquivo. |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `endJob`  |  `xsd:boolean`  | Opcional. O padrão é falso. |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de carregamento) | `uploadParams`  |  `types:UploadPostJob`  | Opcional se esta for uma solicitação subsequente para um trabalho ativo existente. Se houver um trabalho existente, `uploadParams` será ignorado e os parâmetros de carregamento de trabalho existentes serão usados. Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

No bloco `<uploadPostParams>` está o bloco `<uploadParams>` que designa o processamento dos arquivos incluídos.

Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Embora você possa supor que o parâmetro `uploadParams` possa mudar para arquivos individuais como parte do mesmo trabalho, esse não é o caso. Use os mesmos `uploadParams` parâmetros para o trabalho inteiro.

A solicitação POST inicial para um novo trabalho de carregamento deve especificar o parâmetro `jobName`, de preferência usando um nome de trabalho exclusivo para simplificar a sondagem de status de trabalho subsequente e as consultas de log de trabalho. Solicitações POST adicionais para o mesmo trabalho de carregamento devem especificar o parâmetro `jobHandle` em vez de `jobName`, usando o valor `jobHandle` retornado da solicitação inicial.

A solicitação POST final para um trabalho de carregamento deve definir o parâmetro `endJob` como true para que nenhum arquivo futuro seja POST para esse trabalho. Por sua vez, isso permite que a tarefa seja concluída imediatamente após todos os arquivos POSTed serem assimilados. Caso contrário, a tarefa expirará se nenhuma solicitação POST adicional for recebida em 30 minutos.

## Resposta de UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Para uma solicitação POST bem-sucedida, o corpo da resposta é um documento XML `uploadPostReturn`, como o XSD especifica no seguinte:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

O `jobHandle` retornado é passado no parâmetro `uploadPostParams`/ `jobHandle` para qualquer solicitação POST subsequente para o mesmo trabalho. Você também pode usá-lo para sondar o status do trabalho com a operação `getActiveJobs` ou para consultar os logs de trabalho com a operação `getJobLogDetails`.

Se houver um erro ao processar a solicitação POST, o corpo da resposta consistirá em um dos tipos de falha da API, conforme descrito em [Falhas](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemplo de solicitação POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Exemplo de resposta POST - sucesso {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Exemplo de resposta POST - erro {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
