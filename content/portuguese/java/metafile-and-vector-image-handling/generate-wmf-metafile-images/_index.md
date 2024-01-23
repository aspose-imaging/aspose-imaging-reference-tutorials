---
title: Criando imagens WMF com Aspose.Imaging para Java
linktitle: Gerar imagens de metarquivo WMF
second_title: API de processamento de imagem Java Aspose.Imaging
description: Aprenda como criar imagens de metarquivo WMF em Java usando Aspose.Imaging. Siga este guia passo a passo para obter recursos avançados de geração de imagens.
type: docs
weight: 10
url: /pt/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
Você deseja criar imagens WMF (Windows Metafile) com seus aplicativos Java? Aspose.Imaging for Java é uma ferramenta poderosa que permite gerar imagens WMF com facilidade. Neste guia passo a passo, orientaremos você no processo de uso do Aspose.Imaging for Java para criar imagens de metarquivo WMF. 

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos em vigor:

- Um ambiente de desenvolvimento Java configurado em seu computador.
-  Biblioteca Aspose.Imaging para Java instalada. Você pode baixá-lo no[local na rede Internet](https://releases.aspose.com/imaging/java/).
- Conhecimento básico de programação Java.

## Importar pacotes

Primeiro, importe os pacotes necessários para que seu aplicativo Java use Aspose.Imaging for Java:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Etapa 1: crie uma tela

 Para começar a criar sua imagem WMF, você precisa criar uma tela onde possa desenhar formas. O`WmfRecorderGraphics2D` class fornece essa tela. Veja como você pode criar uma instância dele:

```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

No código acima especificamos as dimensões da tela (100x100) e a resolução (96 DPI).

## Etapa 2: definir a cor de fundo

 A seguir, defina a cor de fundo da sua tela. Você pode usar o`setBackgroundColor` método para definir a cor de fundo:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Neste exemplo, definimos a cor de fundo como fumaça branca.

## Etapa 3: definir caneta e pincel

Para desenhar formas na tela, você precisa definir uma caneta e um pincel. A caneta é usada para desenhar contornos e o pincel é usado para preencher formas. Veja como você pode criar uma caneta e um pincel sólido:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Neste código, criamos uma caneta azul e um pincel sólido verde-amarelo.

## Etapa 4: preencher e desenhar formas

Agora vamos preencher e desenhar algumas formas básicas na tela. Começaremos com um polígono:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Aqui, preenchemos e desenhamos um polígono usando a caneta e o pincel especificados. Você pode ajustar as coordenadas e formas conforme necessário.

## Etapa 5: usar o HatchBrush

 Para adicionar texturas às suas formas, você pode usar um`HatchBrush`. Por exemplo:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Neste código, criamos um pincel hachurado com as cores branco e prata.

## Etapa 6: preencher e desenhar uma elipse

Vamos preencher e desenhar uma elipse na tela:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Você pode ajustar a posição e o tamanho da elipse conforme necessário.

## Etapa 7: desenhar arco e Bézier cúbico

Também é possível desenhar formas mais complexas. Veja como desenhar um arco e uma curva cúbica de Bézier:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

No código acima, primeiro desenhamos um arco com um estilo de linha pontilhada e, em seguida, desenhamos uma curva cúbica de Bézier com uma caneta vermelha sólida.

## Etapa 8: adicionar imagens

Você também pode adicionar imagens ao metarquivo WMF. Veja como fazer isso:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Nesta etapa, carregamos uma imagem e a colocamos na tela nas coordenadas especificadas (50, 50).

## Etapa 9: desenhar linhas e torta

Para adicionar linhas e formas de pizza, você pode seguir estes exemplos:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Aqui, desenhamos uma linha e preenchemos/desenhamos uma forma de torta usando a caneta e o pincel especificados.

## Etapa 10: desenhar polilinha e texto

Adicionar texto e polilinhas é simples:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Você pode personalizar a fonte, o texto e os pontos da polilinha conforme necessário.

## Etapa 11: salve a imagem WMF

Depois de criar sua imagem WMF, é hora de salvá-la:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Este código salvará a imagem WMF no diretório especificado.

É isso! Você gerou com êxito uma imagem de metarquivo WMF usando Aspose.Imaging for Java.

## Conclusão

Neste tutorial, exploramos como criar imagens de metarquivo WMF usando Aspose.Imaging for Java. Cobrimos os pré-requisitos necessários, importamos pacotes e fornecemos instruções passo a passo para desenhar várias formas, adicionar texturas, inserir imagens e salvar a imagem final. Aspose.Imaging for Java oferece um poderoso conjunto de ferramentas para manipulação e criação de imagens, tornando-o um recurso valioso para seus aplicativos Java.

## Perguntas frequentes

### Q1: O que é um formato de imagem WMF?

A1: WMF significa Windows Metafile, que é um formato gráfico vetorial usado para armazenar imagens, desenhos e outros dados gráficos. É comumente usado em aplicativos Windows e pode ser facilmente dimensionado sem perda de qualidade.

### Q2: Onde posso baixar o Aspose.Imaging para Java?

 A2: Você pode baixar Aspose.Imaging para Java no[local na rede Internet](https://releases.aspose.com/imaging/java/).

### Q3: Preciso de conhecimentos avançados de programação para usar Aspose.Imaging for Java?

A3: Embora seja necessário conhecimento básico de programação Java, Aspose.Imaging for Java fornece uma API amigável que simplifica a manipulação de imagens e tarefas de criação.

### Q4: Posso usar Aspose.Imaging for Java para fins comerciais?

 A4: Sim, Aspose.Imaging for Java oferece licenças comerciais para empresas e desenvolvedores. Você pode comprar uma licença de[aqui](https://purchase.aspose.com/buy).

### P5: Onde posso obter suporte ou fazer perguntas sobre o Aspose.Imaging for Java?

 A5: Você pode encontrar suporte e interagir com a comunidade Aspose no[Fóruns Aspose.Imaging](https://forum.aspose.com/).