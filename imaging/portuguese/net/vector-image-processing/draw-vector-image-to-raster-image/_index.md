---
title: Desenhe imagem vetorial para imagem raster em Aspose.Imaging for .NET
linktitle: Desenhe imagem vetorial para imagem raster em Aspose.Imaging for .NET
second_title: API de processamento de imagem Aspose.Imaging .NET
description: Aprenda como converter imagens vetoriais em imagens raster em .NET usando Aspose.Imaging. Um guia passo a passo para processamento eficiente de imagens.
weight: 13
url: /pt/net/vector-image-processing/draw-vector-image-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Desenhe imagem vetorial para imagem raster em Aspose.Imaging for .NET


Você deseja converter imagens vetoriais em imagens raster sem esforço em seus aplicativos .NET? Aspose.Imaging for .NET fornece uma solução eficiente para esta tarefa. Neste guia passo a passo, orientaremos você no processo de desenho de imagens vetoriais em imagens raster usando Aspose.Imaging for .NET. 

## Pré-requisitos

Antes de mergulharmos no tutorial, certifique-se de ter os seguintes pré-requisitos em vigor:

### 1. Aspose.Imaging para .NET

 Você deve ter o Aspose.Imaging for .NET instalado. Caso não o tenha, você pode baixá-lo no site em[Baixe Aspose.Imaging para .NET](https://releases.aspose.com/imaging/net/).

### 2. Ambiente de desenvolvimento .NET

Certifique-se de ter um ambiente de desenvolvimento .NET configurado em seu computador. Você pode usar o Visual Studio ou qualquer outra ferramenta de desenvolvimento .NET.

Agora, vamos dividir o processo de desenho de imagens vetoriais em imagens raster em etapas simples e fáceis de seguir:

## Etapa 1: inicialize seu projeto

Comece criando um novo projeto .NET em seu ambiente de desenvolvimento. Certifique-se de ter o Aspose.Imaging for .NET integrado ao seu projeto.

## Etapa 2: carregar a imagem vetorial

Nesta etapa carregamos a imagem vetorial (em formato SVG) que deseja converter em imagem raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Etapa 3: rasterizar a imagem vetorial

Agora precisamos rasterizar a imagem SVG para o formato PNG. É aqui que ocorre a conversão de vetor para raster.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Etapa 4: carregar a imagem raster

Após a rasterização, carregue a imagem PNG do fluxo para desenho posterior.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Etapa 5: desenhe a imagem raster

Agora podemos desenhar a imagem raster na imagem SVG existente.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Etapa 6: salve o resultado

Por fim, salve a imagem resultante. Agora você tem uma imagem raster que inclui sua imagem vetorial.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Conclusão

Neste tutorial, demonstramos como converter imagens vetoriais em imagens raster usando Aspose.Imaging for .NET. Com essas etapas simples, você pode integrar facilmente essa funcionalidade aos seus aplicativos .NET.

### perguntas frequentes

### O que é Aspose.Imaging para .NET?
Aspose.Imaging for .NET é uma biblioteca .NET que fornece recursos poderosos de processamento de imagens, incluindo a capacidade de trabalhar com vários formatos de imagem, converter imagens e executar tarefas avançadas de manipulação de imagens.

### Onde posso encontrar a documentação do Aspose.Imaging for .NET?
 Você pode encontrar a documentação do Aspose.Imaging for .NET[aqui](https://reference.aspose.com/imaging/net/).

### Existe uma versão de teste gratuita disponível?
 Sim, você pode acessar uma avaliação gratuita do Aspose.Imaging for .NET[aqui](https://releases.aspose.com/).

### Como obtenho uma licença temporária do Aspose.Imaging for .NET?
 Se precisar de uma licença temporária, você pode obter uma[aqui](https://purchase.aspose.com/temporary-license/).

### Onde posso obter suporte para Aspose.Imaging for .NET?
 Para qualquer suporte ou dúvida, você pode visitar o[Fórum Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
