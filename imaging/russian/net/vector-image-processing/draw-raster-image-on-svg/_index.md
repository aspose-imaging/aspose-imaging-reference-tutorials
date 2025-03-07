---
title: Как нарисовать растровое изображение в формате SVG в Aspose.Imaging for .NET
linktitle: Рисование растрового изображения в формате SVG в Aspose.Imaging для .NET
second_title: API обработки изображений Aspose.Imaging .NET
description: Узнайте, как рисовать растровые изображения в SVG с помощью Aspose.Imaging для .NET. Улучшите свои приложения .NET с помощью динамических изображений.
weight: 11
url: /ru/net/vector-image-processing/draw-raster-image-on-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как нарисовать растровое изображение в формате SVG в Aspose.Imaging for .NET


В мире .NET-программирования Aspose.Imaging представляет собой надежную и универсальную библиотеку для решения различных задач, связанных с изображениями. Одна из интересных возможностей, которую он предлагает, — это возможность рисовать растровое изображение на холсте SVG. В этом пошаговом руководстве мы покажем вам процесс рисования растрового изображения в формате SVG с помощью Aspose.Imaging для .NET.

## Предварительные условия

Прежде чем мы углубимся в детали, убедитесь, что у вас есть следующие предварительные условия:

-  Aspose.Imaging for .NET: у вас должна быть установлена библиотека. Если нет, вы можете скачать его с сайта[Страница загрузки Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/).

-  Каталог ваших документов: заменить`"Your Document Directory"` с фактическим путем к вашему рабочему каталогу.

Теперь разобьем весь процесс на простые шаги:

## Шаг 1. Импортируйте необходимые пространства имен

Вам необходимо импортировать необходимые пространства имен для работы с Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Шаг 2. Загрузите изображения

- Сначала загрузите растровое изображение, которое вы хотите нарисовать на холсте SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Затем загрузите изображение холста SVG, в котором вы хотите нарисовать растровое изображение.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Шаг 3. Рисование изображения SVG

Теперь вы можете начать рисовать на существующем SVG-изображении. Для этого вам нужно создать экземпляр`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Шаг 4. Нарисуйте растровое изображение

- Определите границы, где вы хотите нарисовать растровое изображение, и укажите исходную область растрового изображения.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Шаг 5: сохраните результат

После рисования растрового изображения на холсте SVG вы можете сохранить полученное изображение:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Заключение

Поздравляем! Вы успешно нарисовали растровое изображение на холсте SVG, используя Aspose.Imaging для .NET. Это может быть невероятно полезно для создания насыщенных и динамичных изображений в ваших .NET-приложениях.

 Для получения дополнительной информации и подробной документации посетите[Документация Aspose.Imaging для .NET](https://reference.aspose.com/imaging/net/).

## Часто задаваемые вопросы

### Что такое Aspose.Imaging для .NET?
   Aspose.Imaging for .NET — это мощная библиотека обработки изображений, которая позволяет разработчикам создавать, манипулировать и конвертировать изображения в различных форматах в приложениях .NET.

### Могу ли я использовать Aspose.Imaging для .NET в коммерческих проектах?
    Да, вы можете использовать Aspose.Imaging for .NET как в коммерческих, так и в некоммерческих проектах. Подробности о лицензировании можно найти на сайте[страница покупки](https://purchase.aspose.com/buy).

### Доступна ли бесплатная пробная версия?
    Да, вы можете получить бесплатную пробную версию Aspose.Imaging для .NET на сайте[здесь](https://releases.aspose.com/).

### Где я могу получить поддержку или задать вопросы?
    Если у вас есть какие-либо вопросы или вам нужна поддержка, вы можете посетить[Форум Aspose.Imaging](https://forum.aspose.com/).

### Как я могу получить временную лицензию на Aspose.Imaging for .NET?
    Вы можете получить временную лицензию[здесь](https://purchase.aspose.com/temporary-license/).



{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
