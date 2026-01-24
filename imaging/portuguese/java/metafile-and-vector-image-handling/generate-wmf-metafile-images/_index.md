---
date: 2026-01-24
description: Aprenda a criar imagens WMF com Aspose.Imaging para Java – um guia passo
  a passo sobre como criar arquivos metafile WMF.
linktitle: Generate WMF Metafile Images
second_title: Aspose.Imaging Java Image Processing API
title: Como criar imagens WMF com Aspose.Imaging para Java
url: /pt/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Como Criar Imagens WMF com Aspose.Imaging para Java

Você está procurando **aprender como criar imagens WMF (Windows Metafile)** com suas aplicações Java? Aspose.Imaging para Java queF**, desde a configuração da para avaliação; uma licença comercial é necessária para produção.  
- **Qual formato de saída é gerado?** Um arquivo WMF ( **Quanto tempo o exemplo básico leva para ser executado?** Normalmente menos de um segundo em um PC moderno.

## Como Criar, estilizar seus gráficos, adicionar formas ou imagens e, finalmente, salvar o arquivo WMF. Entender o processo geral ajuda a adaptar o exemplo aos seus próprios casos de uso ou elementos de UI personalizados.

## Pré‑requisitos

Antes de começar, certifique‑se de que você tem:

- Um ambiente de desenvolvimento Java (JDK 8+ recomendado).  
- Biblioteca Aspose.Imaging para Java instalada. Você pode baixá‑la no [site](https://releases.aspose.com/imaging/java/).  
- Conhecimento básico de programação Java.

## Importar Pacotes

Primeiro, importe os pacotes necessários para que sua aplicação Java use Aspose.Imaging para Java:

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

## Etapa 1: Criar uma Tela de Desenho

Para começar a criar sua imagem WMF, você precisa de uma tela onde possa desenhar formas. A classe `WmfRecorderGraphics2D` fornece essa tela. Veja como criar uma instância dela:

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

No código acima, especificamos as dimensões da tela (100 × 100) e a resolução (96 DPI).

## Etapa método `setBackgroundColor` para definir a cor de fundo:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Neste exemplo definimos a cor de fundo como *white smoke*.

## Etapa 3: Definir Caneta e Pincel

Para desenhar formas na tela, você precisa definir uma caneta e um pincel. A caneta é usada para contornos e o pincel para preenchimento de formas. Veja como criar uma caneta e um pincel sólido:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Neste código, criamos uma caneta azul e um pincel sólido amarelo‑verde.

## Etapa 4: Preencher e Desenhar Formas

Agora, vamos preencher e desenhar algumas formas básicas na tela. Começaremos com um polígono:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Aqui preenchemos e desenhamos um polígono usando a caneta e o pincel especificados. Ajuste as coordenadas para criar qualquer forma que precisar.

## Etapa 5: Usar HatchBrush

Para adicionar texturas às suas formas, você pode usar um `HatchBrush`. Por exemplo:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Neste código, criamos um pincel de hachura cruzada com cores branca e prata.

## Etapa 6: Preencher e Desenhar Elipse

Vamos preencher e desenhar uma elipse na tela:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Você pode ajustar a posição e o tamanho da elipse conforme necessário.

## Etapa 7: Desenhar Arco e Bezier Cúbico

Desenhar formas mais complexas também é possível. Veja como desenhar um arco e uma curva Bezier cúbica:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

No código acima, primeiro desenhamos um arco com estilo de linha pontilhada e, em seguida, uma curva Bezier cúbica com uma caneta vermelha sólida.

## Etapa 8: Adicionar Imagens

Você também pode adicionar imagens ao seu metafile WMF. Veja como fazer isso:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Nesta etapa, carregamos uma imagem e a posicionamos na tela nas coordenadas especificadas (50, 50).

## Etapa 9: Desenhar Linhas e Setores

Para adicionar linhas e formas de setor, siga estes exemplos:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Aqui desenhamos uma linha e preenchemos/desenhamos um setor usando a caneta e o pincel especificados.

## Etapa 10: Desenhar Polilinha e Texto

Adicionar texto e polilinhas é simples:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Você pode personalizar a fonte, o texto e os pontos da polilinha conforme necessário.

## Etapa 11: Salvar a Imagem WMF

Depois de criar sua imagem WMF, é hora de salvá‑la:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Este código salvará a imagem WMF no diretório especificado.

É isso — você gerou com sucesso um metafile WMF usando Aspose.Imaging para Java.

## Conclusão

Neste tutorial exploramos como **criar imagens WMF** com Aspose.Imaging para Java. Cobriram‑se os pré‑requisitos, a importação dos pacotes necessários e cada passo de desenho — de formas básicas a texto e imagens bitmap incorporadas — antes de finalmente salvar o arquivo WMF. Aspose.Imaging para Java oferece um conjunto rico de primitivas de desenho, tornando‑a ideal para gerar gráficos vetoriais programaticamente.

## Perguntas Frequentes

### Q1: O que é o formato de imagem WMF?

A1: WMF significa Windows Metafile, que é um formato de gráficos vetoriais usado para armazenar imagens, desenhos e outros dados gráficos. É amplamente utilizado em aplicações Windows e pode ser dimensionado sem perda de qualidade.

### Q2: Onde posso baixar Aspose.Imaging para Java?

A2: Você pode baixar Aspose.Imaging para Java no [site](https://releases.aspose.com/imaging/java/).

### Q3: Preciso de habilidades avançadas de programação para usar Aspose.Imaging para Java?

A3: Embora seja necessário conhecimento básico de programação Java, Aspose.Imaging para Java fornece uma API amigável que simplifica tarefas de manipulação e criação de imagens.

### Q4: Posso usar Aspose.Imaging para Java para fins comerciais?

A4: Sim, Aspose.Imaging para Java oferece licenças comerciais para empresas e desenvolvedores. Você pode adquirir uma licença [aqui](https://purchase.aspose.com/buy).

### Q5: Onde posso obter suporte ou fazer perguntas sobre Aspose.Imaging para Java?

A5: Você pode encontrar suporte e interagir com a comunidade nos [fóruns Aspose.Imaging](https://forum.aspose.com/).

---

**Últmais recente)  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}