---
description: O Serviço de imagem fornece várias alternativas para renderizar o texto, acessíveis com os comandos text= e textPs=.
seo-description: O Serviço de imagem fornece várias alternativas para renderizar o texto, acessíveis com os comandos text= e textPs=.
seo-title: Formatação de texto
solution: Experience Manager
title: Formatação de texto
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---


# Formatação de texto{#text-formatting}

O Serviço de imagem fornece várias alternativas para renderizar o texto, acessíveis com os comandos text= e textPs=.

`textPs=` fornece um alto nível de semelhança com texto renderizado com Adobe Photoshop e Illustrator. `text=` é razoavelmente compatível com o texto renderizado com o Windows Wordpad.

>[!NOTE]
>
>Além das diferenças listadas em outro lugar, `text=` produz diferenças sutis no texto renderizado quando comparado com `textPs=`. Por exemplo, sublinhados não têm a mesma espessura e posição e itálico sintetizado são renderizados em um ângulo ligeiramente diferente. Se o texto não se ajustar ao espaço disponível, `text=` poderá cortar parcialmente a última linha, enquanto `textPs=` só renderizará as linhas completas.

Todos os comandos de texto aceitam texto formatado com base em um subconjunto da especificação RTF (Rich Text Format). Cada camada de texto pode especificar um comando de texto diferente.

A tabela a seguir lista os principais recursos disponíveis para cada comando de texto:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Recurso</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Consulte também</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatível com Adobe Photoshop </p> </td> 
   <td> <p> not </p> </td> 
   <td> <p> limited </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluir texto em formas arbitrárias </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluxo de texto ao longo de caminhos arbitrários </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Ajuste de cópias </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Ajuste de cópia <p>, <pre>\copyfit</pre>, <pre>\copy fitlines</pre>, <pre>\copy fitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margens da caixa de texto </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificação completa do parágrafo </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justificação da última linha </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Recuo de parágrafo </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Texto de maiúsculas e minúsculas </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Cores de disponibilização de imagem </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vários modos de suavização de borda </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>fluxo de texto superior inferior/direito à esquerda </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Suporte para Photofont® </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>yes </p> </td> 
   <td> Tratamento de fontes </td> 
  </tr> 
  <tr> 
   <td> <p>Dimensionar a camada automaticamente para ajustar o texto </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Suporte a CMYK </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluxo de caracteres da direita para a esquerda </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Desativar quebra automática de texto </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Dimensionar o texto automaticamente para ajustá-lo à camada (por resolução variável) </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

As strings compatíveis com RTF podem ser montadas manualmente ou formatando o texto desejado em um editor de texto ou processador de texto capaz de salvar arquivos RTF. O arquivo RTF pode ser aberto em um editor de texto simples e o conteúdo RTF bruto relevante do arquivo copiado para o URL da solicitação.

Alguns processadores de texto geram arquivos bastante grandes, que incluem preâmbulos substanciais que não são usados pelo Dynamic Media Image Serving. Recomenda-se remover os elementos RTF não utilizados da string antes de passá-la para os comandos de texto.

A codificação de idioma baseada em padrões UTF-8 e ISO é suportada em strings RTF como uma alternativa aos mecanismos de codificação de caracteres RTF padrão. Isso permite que os aplicativos enviem texto que não seja em inglês para o servidor sem o conhecimento da codificação RTF.

Todos os caracteres não compatíveis com HTTP devem ser escapados corretamente, se a string for transmitida via http. Somente &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; precisam ser escapados se a string for incorporada ao campo `catalog::Modifiers` de um registro de catálogo de imagem. Os caracteres de controle, incluindo `<CR>`, `<LF>` e `<TAB>` devem ser sempre removidos.

Os mecanismos de texto do Serviço de imagem interpretam um subconjunto de comandos definidos pela Especificação RTF (Rich Text Format), versão 1.6. Esse subconjunto está focado na formatação de fontes/caracteres, na formatação simples de parágrafos e no suporte a fontes e conjuntos de caracteres internacionais. No momento, não há suporte para construções de formatação mais avançadas, como folhas de estilos e tabelas.

Familiaridade com a especificação RTF (Rich Text Format), conforme publicada pela Microsoft, é necessária ao tentar construir strings de texto codificadas em RTF manualmente.

* [Manuseio de fonte](r-font-handling.md)
* [Tratamento de cores](r-color-handling.md)
* [Ajuste de cópias](r-copy-fitting.md)
* [Camadas de texto](r-text-layers.md)
* [Posicionamento de texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Comandos e palavras-chave RTF suportados](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemplos de codificação RTF](r-rtf-encoding-examples.md)
