---
date: 2026-02-12
description: Узнайте, как создать пустое изображение Aspose и как нарисовать прямоугольник
  в .NET с помощью Aspose.Imaging — быстрый справочник по работе с изображениями в
  ваших .NET‑приложениях.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Создать пустое изображение Aspose – рисовать прямоугольники в .NET
url: /ru/net/basic-drawing/draw-rectangle/
weight: 14
---

 markdown formatting exactly.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Создание пустого изображения Aspose – Рисование прямоугольников в .NET

Создание и манипулирование изображениями в приложениях .NET может показаться сложным, но с Aspose.Imaging вы можете **create blank image Aspose** всего в несколько строк кода, а затем рисовать на нём фигуры. В этом руководстве мы пройдем весь процесс — от создания пустого холста до рисования прямоугольников—чтобы вы могли сразу начать добавлять графику в свои проекты .NET.

## Быстрые ответы
- **Что означает “create blank image Aspose”?** Это создание пустого битмапа с помощью API Aspose.Imaging.  
- **Как нарисовать прямоугольник .net с помощью Aspose?** Используйте метод `Graphics.DrawRectangle` после инициализации объекта `Graphics`.  
- **Какой пакет NuGet требуется?** `Aspose.Imaging` (последняя версия).  
- **Можно ли сохранить изображение как PNG, JPEG или BMP?** Да — просто измените параметры изображения (например, `BmpOptions`, `JpegOptions`).  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для оценки; для продакшна требуется коммерческая лицензия.

## Что такое “create blank image Aspose”?
Создание пустого изображения означает выделение буфера пикселей с заданной шириной, высотой и форматом пикселей. Aspose.Imaging обрабатывает детали низкого уровня, предоставляя готовый к рисованию холст без необходимости работать с GDI+ или System.Drawing.

## Почему использовать Aspose.Imaging для рисования прямоугольников в .NET?
- **Кросс‑платформенный** — работает на Windows, Linux и macOS.  
- **Без нативных зависимостей** — чистый управляемый код, идеально подходит для серверных сред.  
- **Богатый API рисования** — поддерживает кисти, перья, сглаживание и множество типов фигур.  
- **Высокая производительность** — оптимизировано для больших изображений и пакетной обработки.

## Предварительные требования

1. **Aspose.Imaging for .NET** — скачайте его со [страницы загрузки](https://releases.aspose.com/imaging/net/).  
2. **Среда разработки** — Visual Studio, VS Code или любой совместимый с .NET IDE.  
3. **Среда выполнения .NET** — .NET 6+ или .NET Framework 4.7.2+.  

Теперь, когда всё настроено, давайте погрузимся в код.

## Как создать пустое изображение Aspose в .NET?

### Шаг 1: Импортировать необходимые пространства имён

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Эти пространства имён предоставляют доступ к основным классам обработки изображений, типам кистей и параметрам сохранения изображений.

### Шаг 2: Создать пустое изображение (холст)

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

В этом блоке мы:

* Определяем место вывода (`dataDir`).  
* Настраиваем `BmpOptions` для использования 32‑битного формата пикселей.  
* Создаём **blank image** размером 100 × 100 пикселей.  

### Шаг 3: Как нарисовать прямоугольник .net с помощью Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` заполняет холст цветом фона (желтый в этом примере).  
* `DrawRectangle` рисует два прямоугольника — один простым красным пером, другой с синей сплошной кистью — для визуального контраста.

### Шаг 4: Сохранить изображение

```csharp
image.Save();
```

Вызов `Save` записывает битмап в файловую систему, используя ранее определённые параметры.

## Распространённые проблемы и советы

| Проблема | Причина | Решение |
|----------|---------|----------|
| **Пустое изображение отображается черным** | Фон не очищен | Вызовите `graphic.Clear(Color.YourColor)` перед рисованием. |
| **Исключение File not found** | `dataDir` указывает на несуществующую папку | Убедитесь, что каталог существует, или используйте `Path.Combine` с `Environment.CurrentDirectory`. |
| **Неправильные цвета** | Используется `System.Drawing.Color` вместо `Aspose.Imaging.Color` | Всегда импортируйте `Aspose.Imaging.Color`. |
| **Задержка производительности на больших изображениях** | Используется стандартный `BmpOptions` с высоким бит‑на‑пиксель | Переключитесь на `JpegOptions` или `PngOptions` для сжатия. |

## Часто задаваемые вопросы (расширенные)

**Q: Можно ли рисовать другие фигуры, кроме прямоугольников?**  
A: Конечно. Aspose.Imaging предоставляет методы такие как `DrawEllipse`, `DrawLine` и `DrawPolygon`.

**Q: Является ли библиотека бесплатной для коммерческого использования?**  
A: Нет, Aspose.Imaging — коммерческий продукт, но вы можете оценить его с помощью бесплатной пробной версии, доступной [здесь](https://releases.aspose.com/).

**Q: Работает ли это как в Windows, так и в веб‑приложениях?**  
A: Да, тот же код работает в ASP.NET, Blazor и консольных приложениях.

**Q: Как изменить формат вывода на PNG?**  
A: Замените `BmpOptions` на `PngOptions` и соответственно измените расширение файла.

**Q: Где можно найти более подробную документацию?**  
A: Доступ к полной справке API [здесь](https://reference.aspose.com/imaging/net/) и присоединяйтесь к сообществу на [форуме Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Последнее обновление:** 2026-02-12  
**Тестировано с:** Aspose.Imaging 24.12 for .NET  
**Автор:** Aspose