---
"description": "Узнайте, как рисовать растровые изображения на SVG с помощью Aspose.Imaging для .NET. Улучшите свои приложения .NET с помощью динамических изображений."
"linktitle": "Нарисовать растровое изображение на SVG в Aspose.Imaging для .NET"
"second_title": "API обработки изображений Aspose.Imaging .NET"
"title": "Как нарисовать растровое изображение на SVG в Aspose.Imaging для .NET"
"url": "/ru/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Как нарисовать растровое изображение на SVG в Aspose.Imaging для .NET


В мире программирования .NET Aspose.Imaging выступает в качестве надежной и универсальной библиотеки для обработки различных задач, связанных с изображениями. Одной из ее увлекательных возможностей является возможность рисовать растровые изображения на холсте SVG. В этом пошаговом руководстве мы проведем вас через процесс рисования растровых изображений на SVG с помощью Aspose.Imaging для .NET.

## Предпосылки

Прежде чем углубляться в детали, убедитесь, что у вас выполнены следующие предварительные условия:

- Aspose.Imaging для .NET: У вас должна быть установлена библиотека. Если нет, вы можете загрузить ее с [Страница загрузки Aspose.Imaging для .NET](https://releases.aspose.com/imaging/net/).

- Ваш каталог документов: заменить `"Your Document Directory"` с фактическим путем к вашему рабочему каталогу.

Теперь давайте разобьем процесс на простые шаги:

## Шаг 1: Импорт необходимых пространств имен

Для работы с Aspose.Imaging вам необходимо импортировать необходимые пространства имен:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Шаг 2: Загрузите изображения

- Сначала загрузите растровое изображение, которое вы хотите нарисовать на холсте SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Затем загрузите изображение холста SVG там, где вы хотите нарисовать растровое изображение.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Шаг 3: Рисование на SVG-изображении

Теперь вы можете начать рисовать на существующем изображении SVG. Для этого вам нужно создать экземпляр `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Шаг 4: Нарисуйте растровое изображение

- Определите границы, в которых вы хотите нарисовать растровое изображение, и укажите исходную область из растрового изображения.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Шаг 5: Сохраните результат

После рисования растрового изображения на холсте SVG вы можете сохранить полученное изображение:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Заключение

Поздравляем! Вы успешно нарисовали растровое изображение на холсте SVG с помощью Aspose.Imaging для .NET. Это может быть невероятно полезно для создания насыщенных и динамичных изображений в ваших приложениях .NET.

Для получения дополнительной информации и подробной документации посетите [Документация Aspose.Imaging для .NET](https://reference.aspose.com/imaging/net/).

## Часто задаваемые вопросы

### Что такое Aspose.Imaging для .NET?
   Aspose.Imaging для .NET — это мощная библиотека обработки изображений, которая позволяет разработчикам создавать, обрабатывать и конвертировать изображения в различных форматах в приложениях .NET.

### Могу ли я использовать Aspose.Imaging для .NET в коммерческих проектах?
   Да, вы можете использовать Aspose.Imaging for .NET как в коммерческих, так и в некоммерческих проектах. Подробности лицензирования можно найти на [страница покупки](https://purchase.aspose.com/buy).

### Есть ли бесплатная пробная версия?
   Да, вы можете получить бесплатную пробную версию Aspose.Imaging для .NET от [здесь](https://releases.aspose.com/).

### Где я могу получить поддержку или задать вопросы?
   Если у вас есть вопросы или вам нужна поддержка, вы можете посетить [Форум Aspose.Imaging](https://forum.aspose.com/).

### Как получить временную лицензию на Aspose.Imaging для .NET?
   Вы можете получить временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}