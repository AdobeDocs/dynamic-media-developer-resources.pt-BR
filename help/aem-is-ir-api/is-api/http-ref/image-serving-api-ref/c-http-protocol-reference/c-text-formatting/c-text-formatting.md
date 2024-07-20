---
description: O Servidor de imagens fornece várias alternativas para renderizar o texto, acessíveis com os comandos text= e textPs=.
solution: Experience Manager
title: Formatação de texto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# Formatação de texto{#text-formatting}

O Servidor de imagens fornece várias alternativas para renderizar o texto, acessíveis com os comandos text= e textPs=.

O `textPs=` fornece um alto nível de similaridade com o texto renderizado com o Adobe Photoshop e o Illustrator. `text=` é razoavelmente compatível com o texto renderizado com o Windows Wordpad.

>[!NOTE]
>
>Além das diferenças listadas em outro lugar, `text=` produz diferenças sutis no texto renderizado quando comparado com `textPs=`. Por exemplo, os sublinhados não têm a mesma espessura e posição e o itálico sintetizado é renderizado em um ângulo ligeiramente diferente. Se o texto não couber no espaço disponível, `text=` pode cortar parcialmente a última linha, enquanto `textPs=` renderiza apenas linhas completas.

Todos os comandos de texto aceitam texto formatado com base em um subconjunto da especificação RTF (Rich Text Format). Cada camada de texto pode especificar um comando de texto diferente.

A tabela a seguir lista os principais recursos disponíveis para cada comando de texto:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Recurso</b> </th> 
   <th class="entry"> <b> texto=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Consulte também</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatível com Adobe Photoshop </p> </td> 
   <td> <p> não </p> </td> 
   <td> <p> limitado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluxo de texto em formas arbitrárias </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluxo de texto ao longo de caminhos arbitrários </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuste de cópia </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> Copiar ajuste <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margens da caixa de texto </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificação de parágrafo completo </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justificativa da última linha </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Recuo do parágrafo </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Texto em maiúsculas e minúsculas </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\caps, \escapes </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Cores do Servidor de imagens </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vários modos de suavização de borda </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>fluxo de texto superior-inferior/direito-esquerdo </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Suporte para o Photofont® </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> Manuseio de fonte </td> 
  </tr> 
  <tr> 
   <td> <p>Dimensionar automaticamente a camada para ajustar o texto </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Suporte a CMYK </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\cmykcolortbl,\ *\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluxo de caracteres da direita para a esquerda </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Desativar quebra automática de linha </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Dimensionar o texto automaticamente para ajustar-se à camada (variando a resolução) </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

As cadeias de caracteres compatíveis com RTF podem ser montadas manualmente ou formatando o texto desejado em um editor de texto ou processador de texto capaz de salvar arquivos RTF. O arquivo RTF pode então ser aberto em um editor de texto simples, e o conteúdo RTF bruto relevante do arquivo copiado para o URL da solicitação.

Alguns processadores de texto geram arquivos muito grandes, que incluem preâmbulos substanciais que não são usados pelo Dynamic Media Image Serving. É recomendável remover os elementos RTF não utilizados da cadeia de caracteres antes de passá-la para os comandos de texto.

A codificação de idioma com base nos padrões UTF-8 e ISO é suportada em cadeias de caracteres RTF como uma alternativa aos mecanismos de codificação de caracteres RTF padrão. Isso permite que os aplicativos enviem texto em inglês para o servidor sem conhecimento de codificação RTF.

Todos os caracteres compatíveis com não HTTP devem ter escape adequado, se a cadeia de caracteres for transmitida por meio de http. Somente &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; precisarão de escape se a cadeia de caracteres for incorporada ao campo `catalog::Modifiers` de um registro de catálogo de imagens. Os caracteres de controle, incluindo `<CR>`, `<LF>` e `<TAB>`, sempre devem ser removidos.

Os mecanismos de texto do Servidor de imagens interpretam um subconjunto de comandos definidos pela Especificação Rich Text Format (RTF), versão 1.6. Esse subconjunto tem como foco a formatação de fonte/caractere, a formatação de parágrafo simples e o suporte para fontes e conjuntos de caracteres internacionais. Não há suporte para construções de formatação mais avançadas, como folhas de estilos e tabelas, no momento.

É necessária a familiaridade com a Especificação de Formato Rich Text (RTF), conforme publicada pelo Microsoft, ao tentar criar cadeias de texto codificadas em RTF manualmente.

* [Manuseio de fonte](r-font-handling.md)
* [Tratamento de cores](r-color-handling.md)
* [Ajuste de cópia](r-copy-fitting.md)
* [Camadas de texto](r-text-layers.md)
* [Posicionamento do texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Comandos e palavras-chave RTF compatíveis](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemplos de codificação RTF](r-rtf-encoding-examples.md)
