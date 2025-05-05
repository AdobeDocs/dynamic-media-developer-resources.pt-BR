---
title: Referência de comando
description: Esta seção descreve os comandos do protocolo HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Referência de comando{#command-reference}

Esta seção descreve os comandos do protocolo HTTP.

>[!TIP]
>
>Experimente e descubra os benefícios dos modificadores de imagem do Dynamic Media e do Smart Imaging, usando o [_Instantâneo_](https://snapshot.scene7.com/) do Dynamic Media.
>
> O Instantâneo é uma ferramenta de demonstração visual criada para ilustrar o potencial do Dynamic Media para entrega de imagens otimizadas e dinâmicas. Experimente com imagens de teste ou URLs do Dynamic Media, para observar visualmente a saída de vários modificadores de imagem do Dynamic Media e otimizações de Imagem inteligente para o seguinte:
>* Tamanho do arquivo (com entrega WebP e AVIF)
>* Largura de banda de rede
>* DPR (Relação de pixels do dispositivo)
>
>Para saber como é fácil usar o Instantâneo, reproduza o [Vídeo de treinamento do Instantâneo](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=pt-BR) (3 minutos e 17 segundos).


**Somente para Dynamic Media no Adobe Experience Manager** - Além das configurações básicas de imagem disponíveis na interface do usuário, o [!DNL Dynamic Media] no AEM ( [!DNL Adobe Experience Manager]) oferece suporte a várias modificações avançadas de imagem que você pode especificar no campo **Modificadores de Imagem**. Esses parâmetros são definidos abaixo. No entanto, esteja ciente de que a seguinte funcionalidade não é compatível com o Dynamic Media no AEM.

* Comandos de correção de cores: `icc=` e `iccEmbed=`.
* Modelos básicos e comandos de renderização de texto: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandos de localização: `locale=` e `req=xlate`.
* `req=set` não está disponível para uso geral.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Serviços Dynamic Media não essenciais: SVG, renderização de imagem e Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulte também as [Opções de predefinição de imagem](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=pt-BR#dynamic) do Dynamic Media na documentação do AEM 6.5.

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
* [cortar](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [efeito](r-effect.md)
* [effectMask](r-effectmask.md)
* [estender](r-extend.md)
* [ajustar](r-fit.md)
* [girar](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [ocultar](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [camada](r-layer.md)
* [localidade](r-locale.md)
* [mapa](r-map.md)
* [máscara](r-mask.md)
* [maskUse](r-maskuse.md)
* [rede](r-network.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
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
* [opac](r-opac.md)
* [origem](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectiva](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantizar](r-is-http-quantize.md)
* [rect](r-rect.md)
* [solic](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [girar](r-rotate.md)
* [escala](r-is-http-scale.md)
* [scl](r-scl.md)
* [tamanho](r-size-reference.md)
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
