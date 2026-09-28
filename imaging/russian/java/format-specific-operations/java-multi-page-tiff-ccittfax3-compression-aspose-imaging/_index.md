---
date: '2026-09-28'
description: Узнайте, как использовать ccittfax3 compression java для создания многостраничных
  TIFF‑файлов с Aspose.Imaging. Эффективно сканируйте, архивируйте и уменьшайте размер
  файлов в документообороте.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Узнайте пошагово, как использовать ccittfax3 compression java с Aspose.Imaging
  для создания эффективных многостраничных TIFF‑файлов для сканирования и архивирования.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Как создать многостраничный TIFF с ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Как создать многостраничный TIFF с ccittfax3 compression java
url: /ru/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Освоение создания многостраничных TIFF с использованием ccittfax3 compression java с Aspose.Imaging

## Введение

Если вам необходимо архивировать большие объёмы отсканированных документов, одновременно поддерживая небольшие размеры файлов, **ccittfax3 compression java** — это решение номер один. В этом руководстве показано, как генерировать многостраничные TIFF‑файлы с сжатием CCITTFAX3 в Java с помощью Aspose.Imaging. Вы узнаете, почему это сжатие так эффективно для монохромных сканов, как настроить библиотеку и как добавить каждую страницу в виде кадра.

**Что вы узнаете**
- Как добавить Aspose.Imaging в проект Java.
- Как настроить `TiffOptions` для сжатия CCITTFAX3.
- Как создать `TiffImage`, изменить размер исходных изображений и добавить их как кадры.
- Как эффективно сохранить окончательный многостраничный TIFF.

Давайте пройдем полный процесс реализации.

## Быстрые ответы
- **What is the main benefit of CCITTFAX3 compression?** Сокращение размера файла до 80 % для чёрно‑белых сканов.  
- **Which library provides built‑in support?** Aspose.Imaging for Java, версия 25.5+.  
- **Do I need a license for development?** Бесплатная пробная лицензия работает со всеми функциями; платная лицензия требуется для продакшна.  
- **Can I process hundreds of pages?** Да — Aspose.Imaging потоково обрабатывает страницы, поэтому использование памяти остаётся низким.  
- **Is the code compatible with Java 11 and later?** Абсолютно; API ориентировано на Java 8+.

## Что такое ccittfax3 compression java?
`CCITTFAX3` — это без потерь, монохромный алгоритм сжатия, разработанный для факсов и сканированных изображений документов. Он кодирует каждый пиксель одним битом, обеспечивая высокое качество вывода при значительном уменьшении размера файла — часто на 70‑80 % по сравнению с несжатым TIFF. Это делает его идеальным для архивирования чёрно‑белых документов, где необходимо сохранять точность.

## Почему использовать Aspose.Imaging для этой задачи?
Aspose.Imaging поддерживает **100+** форматов ввода и вывода, включая PDF, PNG, JPEG и TIFF. Его потоковая архитектура может обрабатывать **много сотен страниц** TIFF‑файлов без загрузки всего документа в память, что делает его идеальным для масштабных проектов архивирования.

## Требования

- **Java Development Kit (JDK)** 8 или новее установлен.
- **IDE** такой как IntelliJ IDEA или Eclipse.
- **Maven** или **Gradle** для управления зависимостями.
- Базовые знания Java (классы, объекты, коллекции).

## Настройка Aspose.Imaging для Java

Добавьте библиотеку в ваш файл сборки.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Прямое скачивание

Вы также можете скачать последнюю JAR‑файл с [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Приобретение лицензии

Бесплатная пробная лицензия доступна на [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Для продакшна приобретите постоянную лицензию или запросите временную на [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Для подробного использования API см. документацию Aspose.Imaging for Java [documentation](https://reference.aspose.com/imaging/java/).

### Базовая инициализация

После добавления зависимости инициализируйте библиотеку, как показано ниже.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Как настроить ccittfax3 compression java для многостраничного TIFF?

`TiffOptions` — класс, определяющий формат вывода и параметры сжатия для TIFF‑файла. Загрузите объект `TiffOptions` с перечислением `CCITTGroup3FaxCompression`, затем укажите источник выходного файла. Эта двухшаговая конфигурация подготавливает запись для монохромного сжатия и гарантирует, что каждая добавляемая позже страница будет кодироваться алгоритмом CCITTFAX3, что приводит к значительному уменьшению размера при сохранении качества изображения.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Как создать экземпляр TiffImage в Java?

`TiffImage` представляет многостраничный TIFF‑документ в памяти и предоставляет методы для работы с его кадрами. Сначала задайте ширину и высоту, которые будут общими для всех страниц. Затем создайте `TiffImage`, используя ранее созданный `TiffOptions`. Объект `TiffImage` служит контейнером для отдельных кадров, позволяя добавлять, удалять или переупорядочивать страницы перед сохранением окончательного файла.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Как загрузить и изменить размер исходных изображений из папки?

Отфильтруйте целевой каталог по JPEG‑файлам, прочитайте каждое изображение и измените его размер, чтобы он соответствовал холсту TIFF. Изменение размера перед добавлением кадров уменьшает потребление памяти и ускоряет операцию сохранения. Преобразуя каждое исходное изображение к требуемым размерам и формату пикселей, вы гарантируете единообразный макет страниц и избегаете ошибок выполнения при добавлении кадров в TIFF‑документ.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Как добавить каждое изображение как кадр в многостраничный TIFF?

`TiffFrame` — объект, содержащий отдельное изображение страницы и связанные с ним метаданные внутри TIFF. Пройдите по изменённым изображениям, создайте новый `TiffFrame` и добавьте его в `TiffImage`. Каждый кадр становится отдельной страницей в окончательном документе, а библиотека автоматически обновляет необходимые метаданные, такие как количество страниц и смещения, обеспечивая корректную структуру многостраничного TIFF.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Как сохранить окончательный многостраничный TIFF файл?

Вызовите метод `save` у экземпляра `TiffImage`, указав желаемый путь вывода. Библиотека автоматически записывает все кадры с использованием сжатия CCITTFAX3, эффективно потоково записывает данные на диск и закрывает все связанные ресурсы. После завершения операции сохранения полученный файл содержит все страницы с заданным сжатием, готовый к распространению или архивированию.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Практические применения

- **Архивирование документов:** Хранить отсканированные контракты, счета или юридические записи с минимальными затратами на хранение.  
- **Медицинская визуализация:** Сжимать радиологические сканы, сохраняя диагностические детали.  
- **Печатное производство:** Генерировать многостраничные задания для печати, которые принтеры могут обрабатывать напрямую.

## Соображения по производительности

- Используйте `ResizeOptions`, сохраняющие соотношение сторон, чтобы избежать искажения.  
- Закрывайте каждый объект `Image` после добавления его кадра, чтобы освободить нативную память.  
- Для очень больших пакетов обрабатывайте файлы в параллельных потоках и записывайте каждый сегмент TIFF асинхронно.

## Распространённые ошибки и их устранение

- **Неправильный формат пикселей:** CCITTFAX3 работает только с 1‑битными (чёрно‑белыми) изображениями. Преобразуйте цветные изображения в градации серого перед изменением размера.  
- **Утечки памяти:** Всегда вызывайте `dispose()` у временных объектов `Image`; иначе нативные буферы остаются выделенными.  
- **Размер файла не уменьшился:** Убедитесь, что свойство сжатия `TiffOptions` установлено; иначе используется значение по умолчанию (без сжатия).

## Часто задаваемые вопросы

**Q: Можно ли использовать этот подход с цветными изображениями?**  
A: CCITTFAX3 ограничен монохромными данными; для цвета используйте сжатие JPEG или LZW.

**Q: Поддерживает ли Aspose.Imaging потоковую запись для огромных TIFF‑файлов?**  
A: Да — библиотека записывает каждый кадр напрямую в выходной поток, поддерживая низкое потребление памяти даже при тысячах страниц.

**Q: Как программно применить временную лицензию?**  
A: Загрузите файл `.lic` с помощью `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Есть ли способ предварительно просмотреть TIFF перед сохранением?**  
A: Вы можете отрисовать каждый `TiffFrame` в `BufferedImage` и отобразить его в компоненте Swing.

**Q: Какие версии Java официально поддерживаются?**  
A: Aspose.Imaging поддерживает Java 8 до Java 21, включая LTS‑выпуски.

## Заключение

Теперь у вас есть полный, готовый к продакшну рабочий процесс создания многостраничных TIFF‑файлов с **ccittfax3 compression java** с помощью Aspose.Imaging. Следуя приведённым шагам, вы сможете эффективно архивировать огромные коллекции документов, снижая затраты на хранение и сохраняя высокое качество изображений. Исследуйте дополнительные возможности Aspose.Imaging — такие как OCR, работа с метаданными и конвертация форматов — чтобы ещё больше улучшить ваш конвейер обработки документов.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## Связанные руководства

- [Как создать многостраничный TIFF с Aspose.Imaging для Java – Полное руководство](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Как уменьшить размер файлов изображений с помощью сжатия LZW в Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Разделение кадров многостраничного TIFF с Aspose.Imaging для Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}