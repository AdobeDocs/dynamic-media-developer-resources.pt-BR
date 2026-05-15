---
description: Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.
solution: Experience Manager
title: Dados do Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Dados do Source{#source-data}

Os arquivos de dados de origem do Servidor de imagens incluem arquivos de imagem e máscara, fontes e perfis ICC.

Todos os arquivos de dados de origem devem estar acessíveis ao Servidor de imagens. O Servidor de imagens fornece várias alternativas para especificar o local dos arquivos de dados:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catálogo::Caminho|catálogo::MaskPath|icc::ProfilePath|fonte::FontPath|fonte::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> caminho e nome relativos do arquivo de imagem especificados em uma solicitação HTTP do Servidor de Imagens</span> </p></td> 
 </tr> 
</table>

O servidor combina segmentos de caminho da direita para a esquerda até que um caminho de arquivo absoluto seja estabelecido.

Todos os segmentos `*`rootPath`*` podem ser segmentos de caminho vazios, relativos ou absolutos.

`*`catalogPath`*` é um caminho/nome de arquivo absoluto ou relativo. `*`requestPath`*` deve ser um caminho/nome de arquivo relativo.

Os valores `Multiple IS::RootPath` podem ser definidos em ImageServerRegistry.xml (ou por meio da interface do administrador). Isso permite que os arquivos de dados de origem sejam distribuídos em vários sistemas de arquivos. O Servidor de imagens tenta caminhos alternativos na ordem especificada, até que o arquivo de dados seja encontrado.

Novos arquivos de dados de qualquer tipo podem ser adicionados a qualquer momento sem interromper o servidor.
