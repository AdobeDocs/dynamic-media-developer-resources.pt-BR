---
description: comando URL para Visualizador de vídeo.
solution: Experience Manager
title: caption
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# caption{#caption}

comando URL para Visualizador de vídeo.

` caption= *`arquivo`*[,0|1]`

O visualizador oferece suporte para legendas ocultas por meio de arquivos WebVTT hospedados. As dicas e regiões sobrepostas não são suportadas. Os operadores de posicionamento de sinalização compatíveis incluem o seguinte:

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
   <td colname="col4"> <p> Controle o alinhamento do texto. </p> <p>O padrão é <span class="codeph"> intermediário</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posição do texto </p> </td> 
   <td colname="col3"> <p> 0% a 100% </p> </td> 
   <td colname="col4"> <p> Porcentagem de inserção no componente VideoPlayer no início do texto da legenda. </p> <p>O padrão é 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>tamanho da linha </p> </td> 
   <td colname="col3"> <p> 0% a 100% </p> </td> 
   <td colname="col4"> <p> Porcentagem da largura do vídeo usada para legendas. </p> <p>O padrão é 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>posição da linha </p> </td> 
   <td colname="col3"> <p> 0%-100%|inteiro </p> </td> 
   <td colname="col4"> <p> Determina a posição da linha na página. </p> <p>Se for expresso como um número inteiro (sem sinal de porcentagem), então é o número de linhas da parte superior onde o texto é exibido. </p> <p>Se for uma porcentagem (o sinal de porcentagem é o último caractere), o texto da legenda será exibido e essa porcentagem será reduzida na área de exibição. </p> <p>O padrão é 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Outros recursos WebVTT presentes no arquivo WebVTT não são compatíveis, mas não devem interromper as legendas.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> arquivo</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou caminho para o conteúdo da legenda WebVTT. Forneça o arquivo WebVTT pelo ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado da legenda padrão (ativado é <span class="codeph"> 1</span>). </p> </td> 
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

