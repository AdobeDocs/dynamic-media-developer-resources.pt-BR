---
description: Salvar imagem no arquivo.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# saveToFile{#savetofile}

Salvar imagem no arquivo.

`req=saveToFile&name= *`arquivo`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> arquivo</span> </p> </td> 
  <td class="stentry"> <p>Caminho relativo para arquivo de imagem de destino. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervalo de tempo limite (milissegundos). </p></td> 
 </tr> 
</table>

Salva a imagem de resposta em um arquivo no servidor, em vez de retorná-la ao cliente.

Quando a solicitação de salvamento é concluída com sucesso, a solicitação retorna várias propriedades formatadas em Java, incluindo as seguintes:

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
   <td> <p> <span class="codeph">lastUpdated</span> </p> </td> 
   <td> <p> inteiro </p> </td> 
   <td> <p>Hora de criação do arquivo (número de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> inteiro </p> </td> 
   <td> <p> Número de pixels na imagem salva. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> concluído</span> com êxito. </p> </td> 
  </tr> 
 </tbody> 
</table>

Retorna o status de resposta HTTP 200 para êxito e 403 para falha ou tempo limite da solicitação. A resposta tem o tipo MIME `text/plain` e não pode ser armazenada em cache.

Importante Salvar em arquivos deve ser habilitado especificando o caminho para uma pasta gravável existente em `attribute::SavePath`. `saveToFile=` falha se `attribute::SavePath` estiver vazio.

*`file`* é obrigatório e deve ser um caminho relativo combinado com `attribute::SavePath`. O Servidor de imagens não cria pastas. A pasta de destino deve existir no servidor e ter as configurações de permissão apropriadas para que o Servidor de imagens crie arquivos.

`timeout=` é opcional. O tempo limite padrão é de 60.000 ms ou o valor configurado com `PS::SaveTimeout`.
