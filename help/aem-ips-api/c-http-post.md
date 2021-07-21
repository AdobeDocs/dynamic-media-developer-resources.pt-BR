---
description: O upload de ativos no Dynamic Media Classic envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar toda a atividade de log associada aos arquivos carregados.
solution: Experience Manager
title: Upload de ativos por meio de POSTs HTTP no UploadFile Servlet
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Upload de ativos por meio de POSTs HTTP no UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

O upload de ativos no Dynamic Media Classic envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar toda a atividade de log associada aos arquivos carregados.

Use o seguinte URL para acessar o UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Todas as solicitações de POST para um trabalho de upload devem se originar do mesmo endereço IP.

**URLs de acesso para regiões do Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Localização geográfica </p> </th> 
   <th colname="col2" class="entry"> <p>URL de produção </p> </th> 
   <th colname="col3" class="entry"> <p>URL de armazenamento temporário (uso para desenvolvimento e teste pré-produção) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>América do Norte </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Médio Oriente, Ásia </p> </td> 
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

O trabalho de upload consiste em um ou mais POSTs HTTP que usam um `jobHandle` comum para correlacionar o processamento no mesmo trabalho. Cada solicitação é `multipart/form-data` codificada e consiste nas seguintes partes do formulário:

>[!NOTE]
>
>Todas as solicitações de POST para um trabalho de upload devem se originar do mesmo endereço IP.

|  Parte do formulário POST do HTTP  |  Descrição  |
|---|---|
| `auth`  |   Obrigatório. Um documento authHeader XML especificando informações de autenticação e cliente. Consulte **Solicitar autenticação** em [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Opcional. Você pode incluir um ou mais arquivos para fazer upload com cada solicitação de POST. Cada parte do arquivo pode incluir um parâmetro de nome de arquivo no cabeçalho Content-Disposition usado como nome de arquivo de destino no IPS se nenhum parâmetro `uploadPostParams/fileName` for especificado. |

|  Parte do formulário POST do HTTP   |  nome do elemento uploadPostParams   |  Tipo   |  Descrição   |
|---|---|---|---|
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload)   |   `companyHandle`  |  `xsd:string`  | Obrigatório. Lide com a empresa para a qual o arquivo está sendo carregado.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `jobName`  |  `xsd:string`  | `jobName` ou `jobHandle` é necessário. Nome do trabalho de upload.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `jobHandle`  |  `xsd:string`  | `jobName` ou `jobHandle` é necessário. Gerenciar um trabalho de upload iniciado em uma solicitação anterior.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `locale`  |  `xsd:string`  | Opcional. Idioma e código do país para localização.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `description`  |  `xsd:string`  | Opcional. Descrição da tarefa.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `destFolder`  |  `xsd:string`  | Opcional. Caminho da pasta de destino para o prefixo de uma propriedade de nome de arquivo, especialmente para navegadores e outros clientes que podem não suportar caminhos completos em um nome de arquivo.  |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `fileName`  |  `xsd:string`  | Opcional. Nome do arquivo de destino. Substitui a propriedade filename . |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `endJob`  |  `xsd:boolean`  | Opcional. O padrão é false. |
| `uploadParams` (Obrigatório. Um documento XML `uploadParams` especificando os parâmetros de upload) | `uploadParams`  |  `types:UploadPostJob`  | Opcional se for uma solicitação subsequente para um trabalho ativo existente. Se houver um trabalho existente, `uploadParams` será ignorado e os parâmetros de upload do trabalho existentes serão usados. Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

No bloco `<uploadPostParams>` está o bloco `<uploadParams>` que designa o processamento dos arquivos incluídos.

Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Embora você possa supor que o parâmetro `uploadParams` pode ser alterado para arquivos individuais como parte do mesmo trabalho, não é o caso. Use os mesmos parâmetros `uploadParams` para todo o trabalho.

A solicitação POST inicial para um novo trabalho de upload deve especificar o parâmetro `jobName` , preferencialmente usando um nome de trabalho exclusivo para simplificar a pesquisa de status de trabalho subsequente e as consultas de log de trabalho. As solicitações POST adicionais para o mesmo trabalho de upload devem especificar o parâmetro `jobHandle` em vez de `jobName`, usando o valor `jobHandle` retornado da solicitação inicial.

A solicitação POST final para um trabalho de upload deve definir o parâmetro `endJob` como true para que nenhum arquivo futuro seja POSTed para esse trabalho. Por sua vez, isso permite que o trabalho seja concluído imediatamente após todos os arquivos POSTed serem assimilados. Caso contrário, a tarefa expirará se nenhuma solicitação POST adicional for recebida em 30 minutos.

## Resposta de UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Para uma solicitação POST bem-sucedida, o corpo da resposta será um documento XML `uploadPostReturn`, conforme o XSD especifica no seguinte:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

O `jobHandle` retornado é passado no parâmetro `uploadPostParams`/ `jobHandle` para quaisquer solicitações POST subsequentes para o mesmo trabalho. Você também pode usá-lo para pesquisar o status do trabalho com a operação `getActiveJobs` ou para consultar os logs de trabalho com a operação `getJobLogDetails`.

Se houver um erro ao processar a solicitação de POST, o corpo da resposta consiste em um dos tipos de falha da API, conforme descrito em [Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemplo de solicitação de POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```
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

## Exemplo de resposta de POST - sucesso {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Exemplo de resposta de POST - erro {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
