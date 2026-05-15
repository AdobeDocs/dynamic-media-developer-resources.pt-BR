---
title: legenda
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
TQID: 'https://experienceleague.adobe.com/ydZxVPE4iwQMlJLnmCFXeAzkVX2cSGiuDzeNeEi5iaU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 2%

---

# legenda{#caption}

Parâmetro comum a todos os visualizadores.

>[!NOTE]
>
>Esse comando não se aplica ao Visualizador de imagem de vídeo.

` caption= *`arquivo`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou um caminho para o conteúdo de legenda WebVTT. O Servidor de imagens serve o arquivo WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado de legenda padrão. Habilitado é <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esse visualizador oferece suporte a legendas ocultas por meio de arquivos WebVTT hospedados. As legendas especificadas com esse parâmetro se aplicam ao vídeo que vem primeiro em conjuntos de mídia; os vídeos subsequentes são reproduzidos sem legendas. Não há suporte para dicas e regiões sobrepostas. Operadores de posicionamento de sinalização compatíveis:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chave </p> </th> 
   <th colname="col2" class="entry"> <p>Nome </p> </th> 
   <th colname="col3" class="entry"> <p>Valores </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>testar alinhamento </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> esquerda|direita|meio|início|fim </span> </p> </td> 
   <td colname="col4"> <p> Controla o alinhamento do texto. </p> <p>O padrão é <span class="codeph"> meio </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>posição do texto </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentagem de margem interna no componente VideoPlayer para o início do texto da legenda. </p> <p>O padrão é <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">S </span> </p> </td> 
   <td colname="col2"> <p>tamanho da linha </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Porcentagem da largura do vídeo usada para legendas. </p> <p>O padrão é <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posição da linha </p> </td> 
   <td colname="col3"> <p> 0%-100%|inteiro </p> </td> 
   <td colname="col4"> <p> Determina a posição da linha na página. </p> <p>Se for expresso como um número inteiro sem sinal de porcentagem, será o número de linhas da parte superior onde o texto será exibido. </p> <p>Se for expresso como uma porcentagem - o sinal de porcentagem é o último caractere - o texto da legenda será exibido nessa porcentagem abaixo da área de exibição. </p> <p>O padrão é <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se houver outros recursos WebVTT presentes no arquivo WebVTT, eles não serão compatíveis; no entanto, não interrompem a legendagem.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou um caminho para o conteúdo de legenda WebVTT. O arquivo WebVTT é distribuído pelo Servidor de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado de legenda padrão. </p> <p>Habilitado é <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

Nenhum.

## Exemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
