---
title: Opções comuns
description: As opções a seguir podem ser aplicadas independentemente do tipo de sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Opções comuns{#common-options}

As opções a seguir podem ser aplicadas independentemente do tipo de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> cadeia de caracteres </span> </span> </p> </td> 
  <td class="stentry"> <p>Pasta na qual os arquivos de saída devem ser colocados (incluindo o arquivo de log, se <span class="codeph"> -log </span> for especificado). Pode ser um caminho absoluto ou um caminho relativo para o diretório de trabalho atual. A hierarquia de pastas será criada se não existir. No entanto, ela não se aplica ao arquivo especificado com <span class="codeph"> -log </span>. Se não especificado, os arquivos de saída são gravados na pasta em que o <span class="varname"> sourceFile </span> está localizado. Se <span class="varname"> destFile </span> for especificado, ele sempre será gravado nesse local, e <span class="codeph"> -destpath </span> somente se aplica aos arquivos de saída secundários. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -imagem </span> </p> </td> 
  <td class="stentry"> <p>Se especificada, a (primeira) imagem de visualização é extraída da vinheta, uma imagem de painel adequada de um estilo de gabinete ou a primeira imagem de iluminação de um estilo de revestimento de janela. A imagem extraída é salva como um arquivo TIFF de resolução completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -informações </span> </p> </td> 
  <td class="stentry"> <p>Impede a geração de arquivos de destino. Útil para extrair rapidamente atributos de um <span class="varname"> sourceFile </span>. Somente a miniatura opcional ( <span class="codeph"> -largura da miniatura </span>), a imagem ( <span class="codeph"> -imagem </span>) e os arquivos de log ( <span class="codeph"> -log </span>) são gerados. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Seleciona a codificação de JPEG com perdas para dados de imagem em RGB e tons de cinza incorporados no arquivo de saída, em vez de PNG sem perdas. As imagens com alfa (RGBA) são sempre salvas usando a codificação PNG. <span class="varname"> ival </span> especifica a qualidade do JPEG (1...100); recomenda-se 85 ou superior. O padrão é <span class="codeph"> -jpegquality 0 </span>, que seleciona a codificação PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> caminho </span> </span> </p> </td> 
  <td class="stentry"> <p>Cria um arquivo de log com o caminho/nome especificado. Os caminhos completos de todos os arquivos de saída gravados na pasta de destino são gravados no arquivo de log, e algumas configurações adicionais, como informações de versão e avisos ou erros encontrados (consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Saída </a> para obter detalhes). Nenhum arquivo de log será criado se <span class="codeph"> -log </span> não for especificado; nesse caso, toda a saída de texto é gravada em <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Diminua a prioridade do processo <span class="filepath"> vntc </span>. Este processo pode ser usado para que o <span class="filepath"> vntc </span> não ocupe uma CPU inteira durante o processamento de uma vinheta. Ele permite que o sistema operacional dê mais tempo a outros processos mais importantes. <span class="varname"> val </span> especifica a porcentagem de prioridade mais baixa (0..100). O padrão é <span class="codeph"> -lowerpriority 0 </span>, que não diminui a prioridade do processo <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifique a quantidade máxima de memória que <span class="filepath"> vntc </span> tem permissão para usar em bytes. Quando <span class="filepath"> vntc </span> atinge o limite máximo de memória, ele para de ser processado e produz um erro. O <span class="varname"> val </span> especifica o limite máximo de memória em bytes (0.. 3.758.096.384 (3,5 GB). Quando <span class="varname"> val </span> é 0, o limite máximo de memória é desativado. O padrão é <span class="codeph"> -maxmem 3221225472 </span>, o que significa um limite máximo de memória de 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separador " <span class="varname"> cadeia de caracteres </span>" </span> </p> </td> 
  <td class="stentry"> <p>Especifica o separador colocado entre o nome do arquivo e o sufixo de tamanho/resolução para nomes de arquivo de saída gerados automaticamente. O padrão é "-", caso não esteja especificado. Ignorado se <span class="varname"> destFile </span> ou <span class="codeph"> -info </span> for especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -nitidez <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Permite a nitidez de imagens com nova amostra (dimensionada) durante o processamento. Aplica-se somente à nitidez de miniaturas em arquivos no estilo de gabinete. </p> <p>Especifique 0 para desativar a nitidez (padrão), 1 para ativar a nitidez normal, 2 para ativar a máscara de nitidez apenas para brilho ou 3 para ativar a máscara de nitidez para cada componente de cor. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Define o nível de log. O padrão é 1, que gera todas as mensagens informativas, de aviso e de erro. Defina como 0 para desativar todas as mensagens, exceto as de erro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> quantia </span> <span class="varname"> raio </span> <span class="varname"> limite </span> </span> </p> </td> 
  <td class="stentry"> <p>Define os parâmetros de unsharp-masking. Ignorado se <span class="codeph"> -sharpen </span> estiver definido como 0 ou 1; necessário se <span class="codeph"> -sharpen </span> estiver definido como 2 ou 3. A <span class="varname"> quantidade </span> é um valor real no intervalo 0.0...500.0, o <span class="varname"> raio </span> é um valor real no intervalo 0.0...10.0, e o </span> limite <span class="varname"> é um número inteiro de 0 a 255. Consulte a descrição de <span class="codeph"> op_usm= </span> na Referência do protocolo de disponibilização de imagens para obter mais informações. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Validar se a vinheta fornecida é uma vinheta de produção adequada. O <span class="varname"> val </span> representa a versão mínima de arquivo da vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versão <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Versão do arquivo de saída. Se especificado, deve ser 0 ou uma versão de arquivo de vinheta válida (não superior à versão de arquivo padrão). Se definido como 0 ou não especificado, o arquivo de saída é criado usando a versão de arquivo mais atual. Ignorado se <span class="codeph"> -info </span> for especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -informações de versão </span> </p> </td> 
  <td class="stentry"> <p>Retorna as informações de versão deste utilitário. Especifique sem o nome do arquivo e outras opções. </p> </td> 
 </tr> 
</table>
