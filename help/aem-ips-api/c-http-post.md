---
description: O upload de ativos no Scene7 Production System envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar toda a atividade de log associada aos arquivos carregados.
seo-description: O upload de ativos no Scene7 Production System envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar toda a atividade de log associada aos arquivos carregados.
seo-title: Fazer upload de ativos por meio de HTTP POSTs para o UploadFile Servlet
solution: Experience Manager
title: Fazer upload de ativos por meio de HTTP POSTs para o UploadFile Servlet
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# Fazer upload de ativos por meio de HTTP POSTs para o UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

O upload de ativos no Scene7 Production System envolve uma ou mais solicitações HTTP POST que configuram um trabalho para coordenar toda a atividade de log associada aos arquivos carregados.

Use o seguinte URL para acessar o Servlet UploadFile:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

**Acessar URLs para regiões do Scene7**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Localização geográfica </p> </th> 
   <th colname="col2" class="entry"> <p>URL de produção </p> </th> 
   <th colname="col3" class="entry"> <p>URL de armazenamento temporário (use para desenvolvimento e teste pré-produção) </p> </th> 
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

## Fluxo de trabalho do upload {#section-873625b9512f477c992f5cdd77267094}

O trabalho de upload consiste em um ou mais POSTs HTTP que usam um comum `jobHandle` para correlacionar o processamento no mesmo trabalho. Cada solicitação é `multipart/form-data` codificada e consiste nas seguintes partes do formulário:

>[!NOTE]
>
>Todas as solicitações POST para um trabalho de upload devem se originar do mesmo endereço IP.

| Parte do formulário HTTP POST | Descrição ||-|-|`auth`| Obrigatório. Um documento authHeader XML que especifica as informações de autenticação e cliente. Consulte **Solicitar autenticação** em [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Opcional. Você pode incluir um ou mais arquivos para carregar com cada solicitação POST. Cada parte do arquivo pode incluir um parâmetro de nome de arquivo no cabeçalho Content-Disposition usado como o nome de arquivo do público alvo no IPS se nenhum `uploadPostParams/fileName` parâmetro for especificado. |

| Parte de formulário HTTP POST | uploadNome do elemento PostParams | Tipo | Descrição ||-|-|-|-||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de upload) | `companyHandle`|`xsd:string`| Obrigatório. Manuseie a empresa para a qual o arquivo está sendo carregado. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de upload)|`jobName`|`xsd:string`| `jobName` | ou `jobHandle` é obrigatório. Nome do trabalho de upload. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de upload)|`jobHandle`|`xsd:string`| `jobName` | ou `jobHandle` é obrigatório. Manuseie um trabalho de upload iniciado em uma solicitação anterior. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`locale`|`xsd:string`| Opcional. Idioma e código do país para localizações. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`description`|`xsd:string`| Opcional. Descrição da tarefa. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`destFolder`|`xsd:string`| Opcional. Caminho da pasta do Público alvo para prefixo de uma propriedade de nome de arquivo, especialmente para navegadores e outros clientes que podem não suportar caminhos completos em um nome de arquivo. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`fileName`|`xsd:string`| Opcional. Nome do arquivo de público alvo. Substitui a propriedade filename. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`endJob`|`xsd:boolean`| Opcional. O padrão é falso. ||`uploadParams` (Obrigatório. Um `uploadParams` documento XML que especifica os parâmetros de carregamento)|`uploadParams`|`types:UploadPostJob`| Opcional se esta for uma solicitação subsequente para um trabalho ativo existente. Se houver um trabalho existente, ele `uploadParams` será ignorado e os parâmetros de upload do trabalho existentes serão usados. Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Dentro do `<uploadPostParams>` bloco está o `<uploadParams>` bloco que designa o processamento dos arquivos incluídos.

Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Embora você possa supor que o `uploadParams` parâmetro possa ser alterado para arquivos individuais como parte do mesmo trabalho, esse não é o caso. Use os mesmos `uploadParams` parâmetros para a tarefa inteira.

A solicitação POST inicial para um novo trabalho de upload deve especificar o `jobName` parâmetro, de preferência usando um nome de trabalho exclusivo para simplificar a pesquisa subsequente de status de trabalho e os query de log de trabalhos. As solicitações de POST adicionais para o mesmo trabalho de upload devem especificar o `jobHandle` parâmetro em vez de `jobName`, usando o `jobHandle` valor retornado da solicitação inicial.

A solicitação de POST final para um trabalho de upload deve definir o `endJob` parâmetro como true para que nenhum arquivo futuro seja POSTed para esse trabalho. Por sua vez, isso permite que o trabalho seja concluído imediatamente depois que todos os arquivos POSTed forem ingeridos. Caso contrário, a tarefa expirará se nenhuma solicitação POST adicional for recebida dentro de 30 minutos.

## Resposta de UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Para uma solicitação POST bem-sucedida, o corpo da resposta será um `uploadPostReturn` documento XML, conforme especificado pelo XSD no seguinte:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

O `jobHandle` retornado é passado no parâmetro `uploadPostParams`/ `jobHandle` para todas as solicitações POST subsequentes para o mesmo trabalho. Você também pode usá-lo para pesquisar o status da tarefa com a `getActiveJobs` operação ou para query dos logs de trabalho com a `getJobLogDetails` operação.

Se houver um erro ao processar a solicitação POST, o corpo da resposta consistirá em um dos tipos de falha da API, conforme descrito em [Falhas](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exemplo de solicitação POST {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## Exemplo de resposta POST - sucesso {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## Exemplo de resposta POST - erro {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

