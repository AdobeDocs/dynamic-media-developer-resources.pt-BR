---
description: Utilitário de validação de imagem. Esse utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e que o Servidor de imagens possa lê-los sem dificuldade.
solution: Experience Manager
title: validar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# validar{#validate}

Utilitário de validação de imagem. Esse utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos pelo Servidor de imagens sem dificuldade.

Todos os arquivos de imagem não PTIFF devem passar pela validação antes que o arquivo seja disponibilizado para o Servidor de imagens como uma imagem de origem. Imagens PTIFF devem ser validadas após operações de cópia potencialmente não confiáveis.

## Uso {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -qualquer </span> </p> <p>Tipo de arquivo Source; pelo menos um deve ser especificado (qualquer permite os mesmos tipos de arquivo de imagem compatíveis com IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opções </span> </span> </p> </td> 
  <td class="stentry"> <p>Outras opções de comando (veja abaixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> Arquivo de imagem. Nenhum ou mais, separados por espaços. </p> </td> 
 </tr> 
</table>

## Devoluções {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 se bem-sucedido. Se ocorrer um erro, um valor diferente de zero será retornado e os detalhes do erro serão enviados para `stderr`.

## Opções {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica um arquivo de texto separado contendo a lista de arquivos de imagem. Um registro por arquivo. Se <span class="codeph"> -fileList </span> estiver incluído, <span class="varname"> sourceFile </span> não deverá ser especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Habilita a verificação de todo o arquivo de imagem. Por padrão, somente o cabeçalho da imagem é validado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Verifica a validade do perfil de cores incorporado. Por padrão, o perfil do corpo não está marcado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rejeita imagens com 16 bits por componente de imagem. Sempre especificado pelo Servidor de imagens quando ele valida imagens de origem remota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - detalhada </span> </p> </td> 
  <td class="stentry"> <p> Imprime mais informações se a imagem for inválida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - </span> silencioso </p> </td> 
  <td class="stentry"> <p>Desabilita a saída <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>. Somente um status é retornado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Encerra o processamento quando ocorre uma falha de validação de arquivo, mesmo se arquivos adicionais ainda não tiverem sido validados. Por padrão, o processamento continua quando ocorre um erro de validação </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versão </span> </p> </td> 
  <td class="stentry"> <p>Retorna informações de versão para este utilitário. Especifique sem nenhuma outra opção. </p> </td> 
 </tr> 
</table>
