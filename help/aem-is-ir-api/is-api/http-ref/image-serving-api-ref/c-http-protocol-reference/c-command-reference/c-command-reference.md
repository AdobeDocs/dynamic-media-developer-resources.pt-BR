---
description: Esta seção descreve os comandos do protocolo HTTP.
seo-description: Esta seção descreve os comandos do protocolo HTTP.
seo-title: Referência de comando
solution: Experience Manager
title: Referência de comando
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Referência de comando{#command-reference}

Esta seção descreve os comandos do protocolo HTTP.

**Somente** para Dynamic Media no AEM: Além das configurações básicas de imagem disponíveis na interface do usuário,  [!DNL Dynamic Media] em AEM (  [!DNL Adobe Experience Manager]) suporta inúmeras modificações avançadas de imagem que você pode especificar no campo  **Image** Modifiersfield. Esses parâmetros são definidos abaixo. No entanto, lembre-se de que a seguinte funcionalidade não é suportada no Dynamic Media no AEM.

* Comandos de correção de cores: `icc=` e `iccEmbed=`.
* Comandos básicos de formatação e renderização de texto: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandos de localização: `locale=` e `req=xlate`.
* `req=set` não está disponível para uso geral.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Serviços Dynamic Media não principais: SVG, renderização de imagem e Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulte também as [Opções de predefinição de imagem](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) do Dynamic Media na documentação do AEM 6.5.

* [alinhar](r-align.md)
* [âncora](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [cor](r-color-commandref.md)
* [cultura](r-crop.md)
* [RecortarPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [efeito](r-effect.md)
* [effectMask](r-effectmask.md)
* [extensão](r-extend.md)
* [ajuste](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [hide](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [camada](r-layer.md)
* [locale](r-locale.md)
* [mapa](r-map.md)
* [máscara](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_color_balance](r-op-colorbalance.md)
* [op_colorizar](r-op-colorize.md)
* [op_Contraste](r-op-contrast.md)
* [op_growth](r-op-grow.md)
* [op_growthMask](r-op-growmask.md)
* [op_growthMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opaco](r-opac.md)
* [origem](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectiva](r-perspective.md)
* [po](r-pos.md)
* [printRes](r-printres.md)
* [scan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantificar](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [girar](r-rotate.md)
* [escala](r-is-http-scale.md)
* [scl](r-scl.md)
* [tamanho](r-size-reference.md)
* [src](r-src.md)
* [template](r-template.md)
* [texto](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [inteligência](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
