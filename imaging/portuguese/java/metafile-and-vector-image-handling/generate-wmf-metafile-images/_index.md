---
"description": "Aprenda a criar imagens de metarquivo WMF em Java usando Aspose.Imaging. Siga este guia passo a passo para obter recursos avançados de geração de imagens."
"linktitle": "Gerar imagens de metarquivo WMF"
"second_title": "API de processamento de imagens Java Aspose.Imaging"
"title": "Criando imagens WMF com Aspose.Imaging para Java"
"url": "/pt/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Criando imagens WMF com Aspose.Imaging para Java

Deseja criar imagens WMF (Windows Metafile) com seus aplicativos Java? O Aspose.Imaging para Java é uma ferramenta poderosa que permite gerar imagens WMF com facilidade. Neste guia passo a passo, mostraremos como usar o Aspose.Imaging para Java para criar imagens de metarquivo WMF. 

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos em vigor:

- Um ambiente de desenvolvimento Java configurado no seu computador.
- Biblioteca Aspose.Imaging para Java instalada. Você pode baixá-la do site [site](https://releases.aspose.com/imaging/java/).
- Conhecimento básico de programação Java.

## Pacotes de importação

Primeiro, importe os pacotes necessários para que seu aplicativo Java use o Aspose.Imaging for Java:

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

## Etapa 1: Crie uma tela

Para começar a criar sua imagem WMF, você precisa criar uma tela onde possa desenhar formas. `WmfRecorderGraphics2D` A classe fornece esta tela. Veja como você pode criar uma instância dela:

```java
// O caminho para o diretório de documentos.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

No código acima, especificamos as dimensões da tela (100x100) e a resolução (96 DPI).

## Etapa 2: definir a cor de fundo

Em seguida, defina a cor de fundo da sua tela. Você pode usar o `setBackgroundColor` método para definir a cor de fundo:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Neste exemplo, definimos a cor de fundo como fumaça branca.

## Etapa 3: Defina Caneta e Pincel

Para desenhar formas na tela, você precisa definir uma caneta e um pincel. A caneta é usada para desenhar contornos e o pincel para preencher formas. Veja como você pode criar uma caneta e um pincel sólido:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Neste código, criamos uma caneta azul e um pincel sólido amarelo-esverdeado.

## Etapa 4: Preencha e desenhe formas

Agora, vamos preencher e desenhar algumas formas básicas na tela. Começaremos com um polígono:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Aqui, preenchemos e desenhamos um polígono usando a caneta e o pincel especificados. Você pode ajustar as coordenadas e as formas conforme necessário.

## Etapa 5: use o HatchBrush

Para adicionar texturas às suas formas, você pode usar um `HatchBrush`. Por exemplo:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Neste código, criamos um pincel hachurado com cores branca e prata.

## Etapa 6: preencher e desenhar a elipse

Vamos preencher e desenhar uma elipse na tela:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Você pode ajustar a posição e o tamanho da elipse conforme necessário.

## Etapa 7: Desenhe o arco e o Bézier cúbico

Também é possível desenhar formas mais complexas. Veja como desenhar um arco e uma curva de Bézier cúbica:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

No código acima, primeiro desenhamos um arco com um estilo de linha pontilhada e, em seguida, desenhamos uma curva de Bézier cúbica com uma caneta vermelha sólida.

## Etapa 8: Adicionar imagens

Você também pode adicionar imagens ao seu metarquivo WMF. Veja como fazer:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Nesta etapa, carregamos uma imagem e a colocamos na tela nas coordenadas especificadas (50, 50).

## Etapa 9: Desenhe linhas e pizza

Para adicionar linhas e formas de torta, você pode seguir estes exemplos:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Aqui, desenhamos uma linha e preenchemos/desenhamos um formato de torta usando a caneta e o pincel especificados.

## Etapa 10: Desenhe a polilinha e o texto

Adicionar texto e polilinhas é simples:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Você pode personalizar a fonte, o texto e os pontos de polilinha conforme necessário.

## Etapa 11: Salve a imagem WMF

Depois de criar sua imagem WMF, é hora de salvá-la:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Este código salvará a imagem WMF no diretório especificado.

Pronto! Você gerou com sucesso uma imagem de metarquivo WMF usando o Aspose.Imaging para Java.

## Conclusão

Neste tutorial, exploramos como criar imagens de metarquivo WMF usando o Aspose.Imaging para Java. Abordamos os pré-requisitos necessários, importamos pacotes e fornecemos instruções passo a passo para desenhar diversas formas, adicionar texturas, inserir imagens e salvar a imagem final. O Aspose.Imaging para Java oferece um poderoso conjunto de ferramentas para manipulação e criação de imagens, tornando-se um recurso valioso para seus aplicativos Java.

## Perguntas frequentes

### P1: O que é um formato de imagem WMF?

R1: WMF significa Windows Metafile, um formato de gráficos vetoriais usado para armazenar imagens, desenhos e outros dados gráficos. É comumente usado em aplicativos Windows e pode ser facilmente redimensionado sem perda de qualidade.

### P2: Onde posso baixar o Aspose.Imaging para Java?

A2: Você pode baixar o Aspose.Imaging para Java no [site](https://releases.aspose.com/imaging/java/).

### P3: Preciso de habilidades avançadas de programação para usar o Aspose.Imaging para Java?

R3: Embora seja necessário conhecimento básico de programação Java, o Aspose.Imaging for Java fornece uma API amigável que simplifica as tarefas de criação e manipulação de imagens.

### T4: Posso usar o Aspose.Imaging for Java para fins comerciais?

R4: Sim, o Aspose.Imaging for Java oferece licenças comerciais para empresas e desenvolvedores. Você pode adquirir uma licença em [aqui](https://purchase.aspose.com/buy).

### P5: Onde posso obter suporte ou tirar dúvidas sobre o Aspose.Imaging para Java?

A5: Você pode encontrar suporte e se envolver com a comunidade Aspose no [Fóruns Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}