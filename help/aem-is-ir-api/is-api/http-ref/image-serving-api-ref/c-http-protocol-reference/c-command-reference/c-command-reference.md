---
title: Referência de comando
description: Esta seção descreve os comandos do protocolo HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Referência de comando{#command-reference}

Esta seção descreve os comandos do protocolo HTTP.

>[!TIP]
>
>Experimente e descubra os benefícios dos modificadores de imagem da Dynamic Media e do Smart Imaging, usando o Dynamic Media [_Instantâneo_](https://snapshot.scene7.com/).
>
> O Snapshot é uma ferramenta de demonstração visual, projetada para ilustrar o poder do Dynamic Media para a entrega de imagens otimizada e dinâmica. Experimente imagens de teste ou URLs do Dynamic Media para observar visualmente a saída de vários modificadores de imagem do Dynamic Media e otimizações de Smart Imaging para o seguinte:
>* Tamanho do arquivo (com entrega de WebP e AVIF)
>* Largura de banda de rede
>* DPR (Proporção de pixels do dispositivo)
>
>Para saber como é fácil usar o Snapshot, reproduza o [Vídeo de treinamento de instantâneo](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3 minutos e 17 segundos).


**Somente para Dynamic Media no Adobe Experience Manager** - Além das configurações básicas da imagem disponíveis na interface do usuário, [!DNL Dynamic Media] em AEM ( [!DNL Adobe Experience Manager]) suporta várias modificações de imagem avançadas que você pode especificar na **Modificadores de imagem** campo. Esses parâmetros são definidos abaixo. No entanto, esteja ciente de que a seguinte funcionalidade não é compatível com o Dynamic Media no AEM.

* Comandos de correção de cores: `icc=` e `iccEmbed=`.
* Modelos básicos e comandos de renderização de texto: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandos de localização: `locale=` e `req=xlate`.
* `req=set` não está disponível para uso geral.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Serviços Dynamic Media não principais: SVG, Renderização de imagem e Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulte também a Dynamic Media [Opções de predefinição de imagem](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) na documentação do AEM 6.5.

* [alinhar](r-align.md)
* [âncora](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [cultura](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [efeito](r-effect.md)
* [effectiveMask](r-effectmask.md)
* [estender](r-extend.md)
* [ajuste](r-fit.md)
* [virar](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [ocultar](r-hide.md)
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
* [op_contraste](r-op-contrast.md)
* [op_growth](r-op-grow.md)
* [op_growthMask](r-op-growmask.md)
* [op_growthMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_sound](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origem](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectiva](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [scan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantizar](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [gn](r-rgn.md)
* [girar](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [size](r-size-reference.md)
* [src](r-src.md)
* [modelo](r-template.md)
* [texto](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
