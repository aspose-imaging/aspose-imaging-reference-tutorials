---
date: '2026-06-28'
description: Узнайте, как конвертировать ODP в PNG с помощью Aspose.Imaging for Java,
  установить пользовательские шрифты и отключить системные шрифты для точного отображения.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Как конвертировать ODP в PNG с помощью Aspose.Imaging for Java – Руководство
  по пользовательским шрифтам и экспорту
url: /ru/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Как конвертировать ODP в PNG с помощью Aspose.Imaging для Java – Пользовательские шрифты и руководство по экспорту

В современных Java‑приложениях конвертация файлов OpenDocument Presentation (ODP) в изображения PNG высокого качества является распространённой задачей — особенно когда необходимо сохранить фирменный стиль с помощью пользовательских шрифтов. В этом руководстве показано **как конвертировать ODP** в PNG с использованием Aspose.Imaging для Java, объясняется, как задать папку с пользовательскими шрифтами, отключить системные резервные шрифты и точно настроить параметры растеризации для оптимальной производительности.

**Что вы узнаете**
- Как задать пользовательскую директорию шрифтов для конвертации ODP.  
- Как отключить системные альтернативные шрифты, чтобы использовались только выбранные вами гарнитуры.  
- Как экспортировать файл ODP в PNG с точными размерами и настройками шрифтов.  
- Советы по повышению скорости и снижению использования памяти при обработке больших презентаций.

## Быстрые ответы
- **Можно ли использовать Maven для добавления Aspose.Imaging?** Да, добавьте зависимость Maven и выполните `mvn install`.  
- **Нужна ли лицензия для продакшн?** Для неограниченного использования требуется действующая лицензия Aspose.Imaging.  
- **Будут ли учитываться мои пользовательские шрифты?** Установите папку шрифтов и отключите системные альтернативы, чтобы принудительно их использовать.  
- **Какие форматы изображений поддерживаются?** Aspose.Imaging поддерживает более 120 растровых и векторных форматов, включая PNG, JPEG, TIFF и WebP.  
- **Является ли API потокобезопасным?** Да, большинство классов Aspose.Imaging безопасны для одновременного использования, если создавать отдельные экземпляры для каждого потока.

## Что такое “how to convert odp”?
*“How to convert odp”* относится к процессу преобразования файла OpenDocument Presentation в другой формат — обычно PNG — при сохранении макета, шрифтов и визуального качества. Aspose.Imaging для Java предоставляет одно‑методный рабочий процесс, который выполняет эту конвертацию без необходимости внешних инструментов, позволяя разработчикам интегрировать конвертацию непосредственно в свои приложения с минимальным объёмом кода.

## Почему стоит использовать Aspose.Imaging для Java?
Aspose.Imaging поддерживает **более 120 форматов вывода** и может растеризовать многостраничные файлы ODP без загрузки всего документа в память, снижая пиковое использование ОЗУ до 70 % при работе с большими презентациями. Библиотека также предоставляет встроенное управление шрифтами, устраняя необходимость в сторонних движках рендеринга.

## Предварительные требования
- **Библиотеки**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: версия 8 или новее.  
- **IDE**: IntelliJ IDEA, Eclipse или любой совместимый с Java редактор.  
- **Базовые знания**: Java I/O, объектно‑ориентированное программирование и основы работы с изображениями.

## Инструкции по установке

### Maven
Добавьте следующую зависимость в ваш `pom.xml` и выполните `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Добавьте библиотеку в ваш файл `build.gradle` и обновите проект:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Прямое скачивание
Скачайте последнюю JAR‑файл с [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Шаги получения лицензии
Чтобы разблокировать полную функциональность, примените временную или постоянную лицензию:

1. **Free Trial** – Лицензия не требуется, ограниченный набор функций.  
2. **Temporary License** – Запросите её на [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – Приобретите подписку или постоянную лицензию на [Aspose purchase page](https://purchase.aspose.com/buy).

Инициализируйте библиотеку с помощью вашего лицензионного файла:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Как задать пользовательскую директорию шрифтов для конвертации ODP?
`FontSettings` — класс, управляющий ресурсами шрифтов для Aspose.Imaging. Загрузите свои пользовательские шрифты до начала любой обработки изображений. Это гарантирует, что каждый слайд будет использовать точно те гарнитуры, которые вы предоставляете.

Установите путь к папке шрифтов, используя `FontSettings` из Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Определение*: `FontSettings.setFontsFolder` указывает Aspose.Imaging, где искать TrueType и OpenType шрифты в файловой системе.

## Как отключить системные альтернативные шрифты при конвертации ODP?
Отключение системных альтернатив заставляет движок рендеринга игнорировать шрифты, установленные в операционной системе, гарантируя, что используются только предоставленные вами шрифты. Это устраняет неожиданные замены шрифтов, которые могут изменить визуальный вид ваших слайдов.

Отключите системные альтернативы с помощью следующего вызова:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Определение*: `FontSettings.setGetSystemAlternativeFont(false)` заставляет движок использовать только шрифты, находящиеся в указанной вами папке, устраняя неожиданные замены.

## Как экспортировать файл ODP в PNG с указанным шрифтом?
`RasterizationOptions` определяет, как векторные страницы растеризуются в растровые изображения. Комбинируя настройки шрифтов с параметрами растеризации, вы можете управлять DPI, цветом фона и размером страницы для каждого экспортируемого PNG.

Реализуйте метод экспорта, как показано ниже:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Определение*: Класс `RasterizationOptions` управляет DPI, размером страницы и цветом фона для создаваемых PNG‑файлов.

### Распространённые ошибки и решения
- **Отсутствующие файлы шрифтов** – Убедитесь, что каждый `.ttf` или `.otf`, указанный в ODP, присутствует в заданной папке.  
- **Неправильные пути к файлам** – Используйте абсолютные пути или разрешайте относительные пути относительно `System.getProperty("user.dir")`.  
- **Недостаточные права** – Убедитесь, что процесс Java может читать директорию шрифтов и записывать в папку вывода.

## Практические применения
1. **Бренд‑соответствующие наборы слайдов** – Экспортируйте презентации в PNG для публикации в вебе, сохраняя корпоративные шрифты.  
2. **Автоматизированное создание отчетов** – Преобразуйте каждый слайд в изображение для включения в PDF‑отчёты или email‑рассылки.  
3. **Создание архивов наследия** – Сохраняйте содержимое ODP в виде PNG, чтобы обеспечить будущую доступность без необходимости в ODP‑просмотрщиках.

## Соображения по производительности
- Используйте последнюю версию Aspose.Imaging, чтобы воспользоваться улучшениями многопоточной растеризации (до 2× быстрее на 8‑ядерных процессорах).  
- Оборачивайте обработку изображений в блок try‑with‑resources, чтобы гарантировать своевременное освобождение нативных ресурсов.  
- Настраивайте `RasterizationOptions` (например, уменьшайте DPI) при обработке тысяч слайдов, чтобы сбалансировать качество и использование памяти.

## Часто задаваемые вопросы

**Q: Какова минимальная версия Java, требуемая?**  
A: Aspose.Imaging for Java работает с JDK 8 и новее; рекомендуется JDK 11 для долгосрочной поддержки.

**Q: Можно ли конвертировать только выбранные слайды?**  
A: Да, установите `rasterizationOptions.setPageNumber(specificSlideIndex)` перед вызовом `save`.

**Q: Как работать с ODP‑файлами, защищёнными паролем?**  
A: Загрузите файл с помощью `LoadOptions`, включающего пароль, затем продолжайте с теми же настройками шрифтов.

**Q: Влияет ли отключение системных шрифтов на производительность?**  
A: Это слегка повышает скорость, поскольку движок пропускает поиск системных шрифтов, что особенно заметно на машинах с большой коллекцией шрифтов.

**Q: Где можно найти больше примеров кода?**  
A: Изучите официальную [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) для дополнительных сценариев, таких как пакетная конвертация и преобразования изображений.

## Дополнительные ресурсы
- [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Start Your Free Trial](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)  
- [Buy Aspose Licensing](https://purchase.aspose.com/buy)  
- [Apply for a Temporary License](https://purchase.aspose.com/temporary-license/)  

---

**Последнее обновление:** 2026-06-28  
**Тестировано с:** Aspose.Imaging for Java 25.5  
**Автор:** Aspose

## Связанные руководства

- [Конвертировать ODG в PNG с Aspose.Imaging для Java: Полное руководство](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Эффективная конвертация изображений в Java с Aspose.Imaging: Полное руководство](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}