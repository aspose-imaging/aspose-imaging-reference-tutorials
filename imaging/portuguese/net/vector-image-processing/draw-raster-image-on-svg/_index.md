---
"description": "Aprenda a desenhar imagens raster em SVG usando o Aspose.Imaging para .NET. Aprimore seus aplicativos .NET com imagens dinâmicas."
"linktitle": "Desenhar imagem raster em SVG no Aspose.Imaging para .NET"
"second_title": "API de processamento de imagens Aspose.Imaging .NET"
"title": "Como desenhar uma imagem raster em SVG no Aspose.Imaging para .NET"
"url": "/pt/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Como desenhar uma imagem raster em SVG no Aspose.Imaging para .NET


No mundo da programação .NET, o Aspose.Imaging se destaca como uma biblioteca confiável e versátil para lidar com diversas tarefas relacionadas a imagens. Um recurso fascinante que ele oferece é a capacidade de desenhar uma imagem raster em uma tela SVG. Neste guia passo a passo, mostraremos o processo de desenho de uma imagem raster em um SVG usando o Aspose.Imaging para .NET.

## Pré-requisitos

Antes de entrarmos em detalhes, certifique-se de ter os seguintes pré-requisitos em vigor:

- Aspose.Imaging para .NET: Você precisa ter a biblioteca instalada. Caso contrário, você pode baixá-la do site [Página de download do Aspose.Imaging para .NET](https://releases.aspose.com/imaging/net/).

- Seu diretório de documentos: Substituir `"Your Document Directory"` com o caminho real para seu diretório de trabalho.

Agora, vamos dividir o processo em etapas fáceis de seguir:

## Etapa 1: Importar os namespaces necessários

Você precisa importar os namespaces necessários para trabalhar com o Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Etapa 2: Carregue as imagens

- Primeiro, carregue a imagem raster que você deseja desenhar na tela SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Em seguida, carregue a imagem de tela SVG onde você deseja desenhar a imagem raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Etapa 3: Desenhando na imagem SVG

Agora, você pode começar a desenhar na imagem SVG existente. Para fazer isso, você precisa criar uma instância de `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Etapa 4: Desenhe a imagem raster

- Defina os limites onde você deseja desenhar a imagem raster e especifique a região de origem da imagem raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Etapa 5: Salve o resultado

Depois de desenhar a imagem raster na tela SVG, você pode salvar a imagem resultante:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusão

Parabéns! Você desenhou com sucesso uma imagem raster em uma tela SVG usando o Aspose.Imaging para .NET. Isso pode ser incrivelmente útil para criar imagens ricas e dinâmicas em seus aplicativos .NET.

Para obter mais informações e documentação detalhada, visite o [Documentação do Aspose.Imaging para .NET](https://reference.aspose.com/imaging/net/).

## Perguntas frequentes

### O que é Aspose.Imaging para .NET?
   Aspose.Imaging for .NET é uma poderosa biblioteca de processamento de imagens que permite aos desenvolvedores criar, manipular e converter imagens em vários formatos dentro de aplicativos .NET.

### Posso usar o Aspose.Imaging for .NET em projetos comerciais?
   Sim, você pode usar o Aspose.Imaging para .NET em projetos comerciais e não comerciais. Detalhes sobre o licenciamento podem ser encontrados no [página de compra](https://purchase.aspose.com/buy).

### Existe um teste gratuito disponível?
   Sim, você pode obter uma avaliação gratuita do Aspose.Imaging for .NET em [aqui](https://releases.aspose.com/).

### Onde posso obter suporte ou tirar dúvidas?
   Se você tiver alguma dúvida ou precisar de suporte, pode visitar o [Fórum Aspose.Imaging](https://forum.aspose.com/).

### Como posso obter uma licença temporária para o Aspose.Imaging for .NET?
   Você pode obter uma licença temporária em [aqui](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}