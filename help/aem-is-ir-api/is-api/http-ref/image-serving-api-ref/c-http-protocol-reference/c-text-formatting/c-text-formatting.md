---
description: O Image Serving fornece várias alternativas para renderizar texto, acessíveis com os comandos text= e textPs= .
solution: Experience Manager
title: Formatação de texto
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---


# Formatação de texto{#text-formatting}

O Image Serving fornece várias alternativas para renderizar texto, acessíveis com os comandos text= e textPs= .

`textPs=` O fornece um alto nível de similaridade com o texto renderizado com o Adobe Photoshop e o Illustrator. `text=` é razoavelmente compatível com o texto renderizado com o Windows Wordpad.

>[!NOTE]
>
>Além das diferenças listadas em outro lugar, `text=` produz sutis diferenças no texto renderizado quando comparado a `textPs=`. Por exemplo, sublinhados não têm a mesma espessura e posição, e itálico sintetizado é renderizado em um ângulo um pouco diferente. Se o texto não se encaixar no espaço disponível, `text=` poderá cortar parcialmente a última linha, enquanto `textPs=` renderizará apenas as linhas completas.

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
   <td> <p> não </p> </td> 
   <td> <p> limitado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Fluir texto em formas arbitrárias </p> </td> 
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
   <td> <p>Montagem de cópias </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> Ajuste de cópia <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Margens da caixa de texto </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><pre>\margin</pre>, <pre>\margr</pre>, <pre>\margin</pre>, <pre>\margin</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justificação completa do parágrafo </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justificação da última linha </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Recuo de parágrafo </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Todas as maiúsculas e texto de maiúsculas </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Cores do fornecimento de imagens </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Vários modos anti-aliasing </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>fluxo de texto superior inferior/direito à esquerda </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Suporte para Photofont® </p> </td> 
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
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
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
   <td> <p>Dimensionar o texto automaticamente para ajustá-lo à camada (por resolução variável) </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

As strings compatíveis com RTF podem ser montadas manualmente ou formatando o texto desejado em um editor de texto ou processador de texto capaz de salvar arquivos RTF. O arquivo RTF pode então ser aberto em um editor de texto simples e o conteúdo RTF bruto relevante do arquivo copiado para o URL da solicitação.

Alguns processadores de texto geram arquivos muito grandes, que incluem preâmbulos substanciais que não são usados pelo Dynamic Media Image Serving. Recomenda-se remover os elementos RTF não utilizados da string antes de passar a string para os comandos de texto.

A codificação de idioma baseada em padrões UTF-8 e ISO é suportada em strings RTF como uma alternativa aos mecanismos padrão de codificação de caracteres RTF. Isso permite que os aplicativos enviem texto em idioma diferente do inglês para o servidor sem conhecimento da codificação RTF.

Todos os caracteres não compatíveis com HTTP devem ser escapados corretamente, se a sequência de caracteres for transmitida via http. Somente &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; precisam ser evitados se a cadeia de caracteres for incorporada ao campo `catalog::Modifiers` de um registro de catálogo de imagem. Caracteres de controle, incluindo `<CR>`, `<LF>` e `<TAB>` devem ser sempre removidos.

Os mecanismos de texto do Image Serving interpretam um subconjunto de comandos definidos pela Especificação Rich Text Format (RTF), versão 1.6. Esse subconjunto é focado na formatação de fonte/caractere, formatação de parágrafo simples e suporte para fontes e conjuntos de caracteres internacionais. No momento, não há suporte para construções de formatação mais avançadas, como folhas de estilos e tabelas.

Familiaridade com a especificação Rich Text Format (RTF), conforme publicada pela Microsoft, é necessária ao tentar construir strings de texto codificadas em RTF manualmente.

* [Tratamento de fontes](r-font-handling.md)
* [Tratamento de cores](r-color-handling.md)
* [Montagem de cópias](r-copy-fitting.md)
* [Camadas de texto](r-text-layers.md)
* [Posicionamento do texto](r-text-positioning.md)
* [Caracteres reservados](r-reserved-characters.md)
* [Comandos e palavras-chave RTF suportados](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemplos de codificação RTF](r-rtf-encoding-examples.md)
