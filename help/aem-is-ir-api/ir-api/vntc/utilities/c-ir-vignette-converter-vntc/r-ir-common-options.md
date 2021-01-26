---
description: As opções a seguir podem ser aplicadas independentemente do tipo de sourceFile.
seo-description: As opções a seguir podem ser aplicadas independentemente do tipo de sourceFile.
seo-title: Opções comuns
solution: Experience Manager
title: Opções comuns
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# Opções comuns{#common-options}

As opções a seguir podem ser aplicadas independentemente do tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -despath  <span class="varname"> string  </span> </span> </p> </td> 
  <td class="stentry"> <p>Pasta na qual os arquivos de saída devem ser colocados (incluindo o arquivo de log, se <span class="codeph"> -log </span> for especificado). Pode ser um caminho absoluto ou relativo ao diretório de trabalho atual. A hierarquia de pastas será criada se não existir. Não se aplica ao arquivo especificado com <span class="codeph"> -log </span>. Se não for especificado, os arquivos de saída serão gravados na pasta na qual <span class="varname"> sourceFile </span> está localizado. Se <span class="varname"> destFile </span> for especificado, ele sempre será gravado nesse local e <span class="codeph"> -destpath </span> se aplica somente aos arquivos de saída secundários. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image  </span> </p> </td> 
  <td class="stentry"> <p>Se especificado, a (primeira) imagem de visualização é extraída da vinheta, uma imagem de painel adequada de um estilo de gabinete ou a primeira imagem de iluminação de um estilo de revestimento de janela. A imagem extraída é salva como um arquivo TIFF de resolução total. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info  </span> </p> </td> 
  <td class="stentry"> <p>Impede a geração de arquivos de público alvo. Útil para extrair rapidamente atributos de <span class="varname"> sourceFile </span>. Somente a miniatura opcional ( <span class="codeph"> -thumbwidth </span>), a imagem ( <span class="codeph"> -image </span>) e os arquivos de log ( <span class="codeph"> -log </span>) são gerados. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Seleciona a codificação JPEG com perdas para dados de imagem RGB e em escala cinza incorporados ao arquivo de saída, em vez de PNG sem perdas. As imagens com alfa (RGBA) são sempre salvas usando a codificação PNG. <span class="varname"> o campo  </span> especifica a qualidade JPEG (1...100); 85 ou superior é recomendado. O padrão é <span class="codeph"> -jpegquality 0 </span>, que seleciona a codificação PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cria um arquivo de log com o caminho/nome especificado Os caminhos completos de todos os arquivos de saída gravados na pasta de destino são gravados no arquivo de log, bem como algumas configurações adicionais, como informações da versão e quaisquer avisos ou erros encontrados (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Saída </a> para obter detalhes). Nenhum arquivo de log será criado se <span class="codeph"> -log </span> não for especificado; nesse caso, toda a saída de texto é gravada em <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> ival de prioridade baixa  </span> </span> </p> </td> 
  <td class="stentry"> <p>Diminua a prioridade do processo <span class="filepath"> vntc </span>. Isso pode ser usado para que <span class="filepath"> vntc </span> não assuma uma CPU inteira durante o processamento de uma vinheta. Permite que o sistema operacional dê mais tempo a outros processos mais importantes. <span class="varname"> o Vículo  </span> especifica a porcentagem de prioridade mais baixa (0..100). O padrão é <span class="codeph"> -lowerpriority 0 </span>, o que não diminui a prioridade do processo <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique a quantidade máxima de memória que <span class="filepath"> vntc </span> tem permissão para utilizar em bytes. Quando <span class="filepath"> vntc </span> atinge o limite máximo de memória, ele interrompe o processamento e gera um erro. <span class="varname"> o VAL  </span> especifica o limite máximo de memória em bytes (0... 3.758.096.384 (3,5 GB). Quando <span class="varname"> o valor ival </span> for 0, o limite máximo de memória será desativado. O padrão é <span class="codeph"> -maxmem 322125472 </span>, o que significa um limite máximo de memória de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Especifica o separador colocado entre o nome do arquivo e o sufixo tamanho/resolução para nomes de arquivos de saída gerados automaticamente. O padrão é "-" se não for especificado. Ignorado se <span class="varname"> destFile </span> ou <span class="codeph"> -info </span> for especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -  <span class="varname"> frasco para injetáveis com nitidez  </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite a nitidez de imagens reamostradas (dimensionadas) durante o processamento. Aplica-se somente à nitidez de miniaturas no caso de arquivos no estilo gabinete. </p> <p>Especifique 0 para desativar a nitidez (padrão), 1 para ativar a nitidez normal, 2 para ativar a máscara de nitidez somente para brilho ou 3 para ativar a máscara de nitidez para cada componente de cor. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -traconze  </span> </p> </td> 
  <td class="stentry"> <p>Define o nível do log. O padrão é 1, que gera todas as mensagens informativas, de aviso e de erro. Defina como 0 para desativar todas as mensagens, exceto as de erro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> limite de  </span> <span class="varname"> raio de  </span> <span class="varname"> quantidade usm  </span> </span> </p> </td> 
  <td class="stentry"> <p>Define os parâmetros de máscara de nitidez. Ignorado se <span class="codeph"> -sharpen </span> estiver definido como 0 ou 1; obrigatório se <span class="codeph"> -sharpen </span> estiver definido como 2 ou 3. <span class="varname"> amount  </span> é um valor real no intervalo 0.0...500.0,  <span class="varname"> radius  </span> é um valor real no intervalo 0.0..10.0 e  <span class="varname"> limit  </span> é um número inteiro entre 0 e 255. Consulte a descrição de <span class="codeph"> op_usm= </span> na Referência do protocolo de disponibilização de imagem para obter mais informações. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valide se a vinheta fornecida é uma vinheta de produção adequada. <span class="varname"> o Vírgula  </span> representa a versão mínima do arquivo da vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versão  <span class="varname"> do vídeo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versão do arquivo de saída. Se especificado, deve ser 0 ou uma versão de arquivo de vinheta válida (não maior que a versão de arquivo padrão). Se definido como 0 ou não especificado, o arquivo de saída será criado usando a versão mais recente do arquivo. Ignorado se <span class="codeph"> -info </span> for especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Retorna as informações de versão deste utilitário. Especifique sem nome de arquivo e outras opções. </p> </td> 
 </tr> 
</table>

