---
title: Сжатие DICOM в Aspose.Imaging для .NET
linktitle: Сжатие DICOM в Aspose.Imaging для .NET
second_title: API обработки изображений Aspose.Imaging .NET
description: Узнайте, как выполнить сжатие DICOM с помощью Aspose.Imaging для .NET. Следуйте этому пошаговому руководству, чтобы эффективно хранить и передавать медицинские изображения с высоким диагностическим качеством.
weight: 17
url: /ru/net/dicom-image-processing/dicom-compression/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сжатие DICOM в Aspose.Imaging для .NET

В мире медицинской визуализации стандарт DICOM (цифровая визуализация и связь в медицине) имеет первостепенное значение для хранения и обмена медицинскими изображениями. Aspose.Imaging for .NET, мощная библиотека .NET, обеспечивает комплексную поддержку работы с изображениями DICOM. Это руководство проведет вас через процесс сжатия DICOM с помощью Aspose.Imaging for .NET. Мы разберем каждый шаг и подробно объясним процесс.

## Предварительные условия

Прежде чем мы углубимся в сжатие DICOM с помощью Aspose.Imaging for .NET, вам необходимо убедиться, что у вас есть следующие предварительные условия:

1. Визуальная Студия

Убедитесь, что в вашей системе установлена Visual Studio. Если нет, то вы можете скачать его с сайта.

2. Aspose.Imaging для .NET

У вас должна быть библиотека Aspose.Imaging for .NET. Вы можете получить эту библиотеку, перейдя по ссылкам, представленным ниже:

- [Скачать Aspose.Imaging для .NET](https://releases.aspose.com/imaging/net/)
- [Купить Aspose.Imaging для .NET](https://purchase.aspose.com/buy)
- [Получите бесплатную пробную лицензию](https://releases.aspose.com/)
- [Временная лицензия](https://purchase.aspose.com/temporary-license/)

Имея все эти предварительные условия, давайте перейдем к пошаговому руководству по выполнению сжатия DICOM с помощью Aspose.Imaging for .NET.

## Импортировать пространства имен

Прежде чем продолжить, нам необходимо импортировать необходимые пространства имен для доступа к необходимым классам и методам. Откройте проект Visual Studio и в верхней части файла C# добавьте следующее:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Теперь мы готовы начать процесс сжатия DICOM.

## Шаг 1. Загрузите исходное изображение

 Начнем с загрузки исходного изображения, которое вы хотите преобразовать в формат DICOM. Обязательно замените`"Your Document Directory"` с фактическим путем к каталогу вашего изображения.

```csharp
string dataDir = "Your Document Directory";
string inputFile = Path.Combine(dataDir, "original.jpg");

using (var inputImage = Image.Load(inputFile))
{
    // Здесь будет находиться ваш код сжатия DICOM.
}
```

## Шаг 2. Выполните несжатое сжатие DICOM.

На этом этапе мы выполним несжатое сжатие DICOM. Вот код для этого:

```csharp
string output1 = Path.Combine(dataDir, "original_Uncompressed.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.None }
};

inputImage.Save(output1, options);
```

## Шаг 3. Выполните сжатие JPEG DICOM.

Теперь перейдем к сжатию DICOM с использованием формата JPEG:

```csharp
string output2 = Path.Combine(dataDir, "original_JPEG.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Jpeg }
};

inputImage.Save(output2, options);
```

## Шаг 4. Выполните сжатие JPEG2000 DICOM.

На этом этапе мы выполним сжатие DICOM с использованием формата JPEG2000. Вот как это сделать:

```csharp
string output3 = Path.Combine(dataDir, "original_JPEG2000.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression
    {
        Type = CompressionType.Jpeg2000,
        Jpeg2000 = new Jpeg2000Options
        {
            Codec = Jpeg2000Codec.Jp2,
            Irreversible = false
        }
    }
};

inputImage.Save(output3, options);
```

## Шаг 5. Выполните сжатие RLE DICOM.

Наконец, давайте выполним сжатие DICOM с использованием формата RLE (кодирование длины):

```csharp
string output4 = Path.Combine(dataDir, "original_RLE.dcm");

var options = new DicomOptions
{
    ColorType = ColorType.Rgb24Bit,
    Compression = new Compression { Type = CompressionType.Rle }
};

inputImage.Save(output4, options);
```

## Заключение

 В этом пошаговом руководстве мы узнали, как выполнять сжатие DICOM с помощью Aspose.Imaging для .NET. Эта библиотека предоставляет мощный набор инструментов для работы с медицинскими изображениями. Более подробно ее возможности можно изучить, обратившись к[документация](https://reference.aspose.com/imaging/net/).

## Часто задаваемые вопросы

### Вопрос 1. Что такое сжатие DICOM?

A1: Сжатие DICOM — это процесс уменьшения размера медицинских изображений при сохранении их диагностического качества. Это важно для эффективного хранения и передачи медицинских данных.

### Вопрос 2. Зачем использовать Aspose.Imaging for .NET для сжатия DICOM?

A2: Aspose.Imaging for .NET предлагает надежный набор функций и удобный API для работы с изображениями DICOM, что делает его отличным выбором для приложений медицинской визуализации.

### Вопрос 3. Могу ли я применять другие операции обработки изображений в сочетании со сжатием DICOM с помощью Aspose.Imaging for .NET?

О3: Да, Aspose.Imaging for .NET предоставляет широкий спектр возможностей обработки изображений, которые можно комбинировать со сжатием DICOM для удовлетворения конкретных требований.

### Вопрос 4. Где я могу получить поддержку или задать вопросы, связанные с Aspose.Imaging for .NET?

 A4: Вы можете посетить[Форумы Aspose.Imaging](https://forum.aspose.com/) чтобы получить поддержку, задать вопросы и пообщаться с сообществом Aspose.Imaging.

### Вопрос 5: Существует ли пробная версия Aspose.Imaging для .NET, доступная для тестирования?

 A5: Да, вы можете получить[бесплатная пробная лицензия](https://releases.aspose.com/) протестировать Aspose.Imaging для .NET перед покупкой.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
