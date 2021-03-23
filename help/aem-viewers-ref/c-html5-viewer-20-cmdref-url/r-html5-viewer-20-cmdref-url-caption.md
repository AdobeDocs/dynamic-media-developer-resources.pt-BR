---
description: Parâmetro comum a todos os visualizadores.
seo-description: Parâmetro comum a todos os visualizadores.
seo-title: caption
solution: Experience Manager
title: caption
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# caption{#caption}

Parâmetro comum a todos os visualizadores.

>[!NOTE]
>
>Este comando não se aplica ao Visualizador de imagem de vídeo.

` caption= *`arquivo`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou caminho para o conteúdo da legenda WebVTT. O Serviço de Imagens serve o arquivo WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado da legenda padrão. Ativado é <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Este visualizador oferece suporte a legendas ocultas por meio de arquivos WebVTT hospedados. As legendas especificadas com esse parâmetro se aplicam ao vídeo que vem primeiro em conjuntos de mídia; os vídeos subsequentes são reproduzidos sem legendas. As dicas e regiões sobrepostas não são suportadas. Operadores de posicionamento de sinalização compatíveis:

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
   <td colname="col1"> <p> <span class="codeph"> A  </span> </p> </td> 
   <td colname="col2"> <p>alinhamento de teste </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> esquerda|direita|meio|início|fim  </span> </p> </td> 
   <td colname="col4"> <p> Controla o alinhamento do texto. </p> <p>O padrão é <span class="codeph"> intermediário </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T  </span> </p> </td> 
   <td colname="col2"> <p>posição do texto </p> </td> 
   <td colname="col3"> <p> 0% a 100% </p> </td> 
   <td colname="col4"> <p> Porcentagem de inserção no componente VideoPlayer no início do texto da legenda. </p> <p>O padrão é <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>tamanho da linha </p> </td> 
   <td colname="col3"> <p> 0% a 100% </p> </td> 
   <td colname="col4"> <p> Porcentagem da largura do vídeo usada para legendas. </p> <p>O padrão é <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L  </span> </p> </td> 
   <td colname="col2"> <p>posição da linha </p> </td> 
   <td colname="col3"> <p> 0%-100%|inteiro </p> </td> 
   <td colname="col4"> <p> Determina a posição da linha na página. </p> <p>Se for expresso como um número inteiro sem sinal de porcentagem, então é o número de linhas da parte superior onde o texto é exibido. </p> <p>Se for expresso como uma porcentagem - o sinal de porcentagem é o último caractere - o texto da legenda será exibido, aquele percentual abaixo da área de exibição. </p> <p>O padrão é <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esteja ciente de que, se houver outros recursos WebVTT presentes no arquivo WebVTT, eles não são suportados; no entanto, elas não interromperão as legendas.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou caminho para o conteúdo da legenda WebVTT. O arquivo WebVTT é disponibilizado pelo Serviço de Imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Especifica o estado da legenda padrão. </p> <p>Ativado é <span class="codeph"> 1 </span>. </p> </td> 
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

