---
title: Como desenhar uma imagem raster em SVG no Aspose.Imaging for .NET
linktitle: Desenhe imagem raster em SVG em Aspose.Imaging for .NET
second_title: API de processamento de imagem Aspose.Imaging .NET
description: Aprenda como desenhar imagens raster em SVG usando Aspose.Imaging for .NET. Aprimore seus aplicativos .NET com imagens dinâmicas.
type: docs
weight: 11
url: /pt/net/vector-image-processing/draw-raster-image-on-svg/
---

No mundo da programação .NET, Aspose.Imaging se destaca como uma biblioteca confiável e versátil para lidar com várias tarefas relacionadas a imagens. Um recurso fascinante que oferece é a capacidade de desenhar uma imagem rasterizada em uma tela SVG. Neste guia passo a passo, orientaremos você no processo de desenho de uma imagem raster em um SVG usando Aspose.Imaging for .NET.

## Pré-requisitos

Antes de nos aprofundarmos nos detalhes, certifique-se de ter os seguintes pré-requisitos em vigor:

-  Aspose.Imaging for .NET: Você deve ter a biblioteca instalada. Caso contrário, você pode baixá-lo no[Página de download do Aspose.Imaging para .NET](https://releases.aspose.com/imaging/net/).

-  Seu diretório de documentos: Substitua`"Your Document Directory"` com o caminho real para o seu diretório de trabalho.

Agora, vamos dividir o processo em etapas fáceis de seguir:

## Etapa 1: importar namespaces necessários

Você precisa importar os namespaces necessários para trabalhar com Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Etapa 2: carregar as imagens

- Primeiro, carregue a imagem raster que deseja desenhar na tela SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Em seguida, carregue a imagem da tela SVG onde deseja desenhar a imagem raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Etapa 3: desenhar na imagem SVG

Agora você pode começar a desenhar na imagem SVG existente. Para fazer isso, você precisa criar uma instância de`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Etapa 4: desenhe a imagem raster

- Defina os limites onde deseja desenhar a imagem raster e especifique a região de origem da imagem raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Etapa 5: salve o resultado

Depois de desenhar a imagem raster na tela SVG, você pode salvar a imagem resultante:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusão

Parabéns! Você desenhou com sucesso uma imagem raster em uma tela SVG usando Aspose.Imaging for .NET. Isso pode ser extremamente útil para criar imagens ricas e dinâmicas em seus aplicativos .NET.

 Para mais informações e documentação detalhada, visite o[Documentação do Aspose.Imaging para .NET](https://reference.aspose.com/imaging/net/).

## perguntas frequentes

### O que é Aspose.Imaging para .NET?
   Aspose.Imaging for .NET é uma poderosa biblioteca de processamento de imagens que permite aos desenvolvedores criar, manipular e converter imagens em vários formatos em aplicativos .NET.

### Posso usar o Aspose.Imaging for .NET em projetos comerciais?
    Sim, você pode usar Aspose.Imaging for .NET em projetos comerciais e não comerciais. Detalhes de licenciamento podem ser encontrados no site[página de compra](https://purchase.aspose.com/buy).

### Existe um teste gratuito disponível?
    Sim, você pode obter uma avaliação gratuita do Aspose.Imaging for .NET em[aqui](https://releases.aspose.com/).

### Onde posso obter suporte ou tirar dúvidas?
    Se você tiver alguma dúvida ou precisar de suporte, você pode visitar o[Fórum Aspose.Imaging](https://forum.aspose.com/).

### Como posso obter uma licença temporária do Aspose.Imaging for .NET?
    Você pode obter uma licença temporária em[aqui](https://purchase.aspose.com/temporary-license/).


