---
description: Salve a imagem no arquivo.
seo-description: Salve a imagem no arquivo.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# saveToFile{#savetofile}

Salve a imagem no arquivo.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> arquivo</span> </p> </td> 
  <td class="stentry"> <p>Caminho relativo para o arquivo de imagem do público alvo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalo de tempo limite (milissegundos). </p></td> 
 </tr> 
</table>

Salva a imagem de resposta em um arquivo no servidor em vez de retorná-la ao cliente.

Quando a solicitação de salvamento é concluída com êxito, a solicitação retorna várias propriedades formatadas em Java, incluindo as seguintes:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Propriedade</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdates</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Hora de criação do arquivo (número de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Número de pixels na imagem salva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> se </span> for bem-sucedido. </p> </td> 
  </tr> 
 </tbody> 
</table>

Retorna o status de resposta HTTP 200 se bem-sucedido e 403 se a solicitação falhar ou expirar. A resposta tem o tipo MIME `text/plain` e não pode ser obtida em cache.

Importante Salvar em arquivos deve ser ativado especificando o caminho para uma pasta gravável existente em `attribute::SavePath`. `saveToFile=` falha se  `attribute::SavePath` estiver vazio.

*`file`* é obrigatório e deve ser um caminho relativo combinado com  `attribute::SavePath`. O Serviço de Imagens não cria pastas. A pasta público alvo deve existir no servidor e ter as configurações de permissão apropriadas para que o Serviço de imagem crie arquivos.

`timeout=` é opcional. O tempo limite padrão é de 60.000 ms, ou qualquer valor configurado com `PS::SaveTimeout`.
