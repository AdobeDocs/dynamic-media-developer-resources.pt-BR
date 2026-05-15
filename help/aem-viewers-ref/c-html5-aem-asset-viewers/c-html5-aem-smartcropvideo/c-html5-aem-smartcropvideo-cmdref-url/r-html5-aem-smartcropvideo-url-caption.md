---
title: legenda
description: Comando de URL para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d7000d0-9181-4c6e-a94e-31ab5ad17fa4
TQID: 'https://experienceleague.adobe.com/yh1XHiqp8t6dB8AjQ769yMSBs0ew5x5dERv-8buuZ4k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# legenda{#caption}

Comando de URL para o Visualizador de Corte inteligente de vídeo.

` caption= *`arquivo`*[,0|1]`

O visualizador é compatível com legendas ocultas por meio de arquivos WebVTT hospedados. Não há suporte para dicas e regiões sobrepostas. Os operadores de posicionamento de sinalização compatíveis incluem o seguinte:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chave </p> </th> 
   <th colname="col2" class="entry"> <p>Nome </p> </th> 
   <th colname="col3" class="entry"> <p>Valor </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>alinhamento de texto </p> </td> 
   <td colname="col3"> <p><span class="codeph"> esquerda|direita|meio|início|fim</span> </p> </td> 
   <td colname="col4"> <p> Controle o alinhamento do texto. </p> <p>O padrão é <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posição do texto </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentagem de margem interna no componente VideoPlayer para o início do texto da legenda. </p> <p>O padrão é 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>tamanho da linha </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentagem da largura do vídeo usada para legendas. </p> <p>O padrão é 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>posição da linha </p> </td> 
   <td colname="col3"> <p> 0%-100%|inteiro </p> </td> 
   <td colname="col4"> <p> Determina a posição da linha na página. </p> <p>Se for expresso como um número inteiro (sem sinal de porcentagem), será o número de linhas da parte superior onde o texto será exibido. </p> <p>Se for uma porcentagem (o sinal de porcentagem é o último caractere), o texto da legenda será exibido nessa porcentagem abaixo da área de exibição. </p> <p>O padrão é 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Outros recursos de WebVTT presentes no arquivo WebVTT não são compatíveis, mas não devem interromper as legendas.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> arquivo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou um caminho para o conteúdo de legenda WebVTT. Disponibilize o arquivo WebVTT pelo ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado de legenda padrão (habilitado é <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

Nenhum.

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
