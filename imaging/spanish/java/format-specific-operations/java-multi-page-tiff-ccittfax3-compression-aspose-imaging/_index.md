---
date: '2026-09-28'
description: Aprenda a usar ccittfax3 compression java para crear archivos TIFF multipágina
  con Aspose.Imaging. Escanee, archive y reduzca el tamaño de archivo de manera eficiente
  para flujos de trabajo de documentos.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Descubra paso a paso cómo usar ccittfax3 compression java con Aspose.Imaging
  para crear archivos TIFF multipágina eficientes para escaneo y archivo.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Cómo crear TIFF multipágina con ccittfax3 compression java
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
title: Cómo crear TIFF multipágina con ccittfax3 compression java
url: /es/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dominar la creación de TIFF multipágina con compresión ccittfax3 java usando Aspose.Imaging

## Introducción

Si necesita archivar grandes volúmenes de documentos escaneados mientras mantiene los tamaños de archivo bajos, **ccittfax3 compression java** es la solución ideal. Este tutorial le muestra cómo generar archivos TIFF multipágina con compresión CCITTFAX3 en Java usando Aspose.Imaging. Aprenderá por qué esta compresión funciona tan bien para escaneos monocromos, cómo configurar la biblioteca y cómo agregar cada página como un marco.

**Lo que aprenderá**
- Cómo agregar Aspose.Imaging a un proyecto Java.
- Cómo configurar `TiffOptions` para compresión CCITTFAX3.
- Cómo crear un `TiffImage`, redimensionar imágenes de origen y agregarlas como marcos.
- Cómo guardar el TIFF multipágina final de manera eficiente.

Recorramos la implementación completa.

## Respuestas rápidas
- **¿Cuál es el principal beneficio de la compresión CCITTFAX3?** Reducción de hasta el 80 % del tamaño del archivo para escaneos en blanco y negro.  
- **¿Qué biblioteca ofrece soporte incorporado?** Aspose.Imaging para Java, versión 25.5+.  
- **¿Necesito una licencia para desarrollo?** Una licencia de prueba gratuita funciona para todas las funciones; se requiere una licencia de pago para producción.  
- **¿Puedo procesar cientos de páginas?** Sí—Aspose.Imaging transmite páginas, por lo que el uso de memoria se mantiene bajo.  
- **¿El código es compatible con Java 11 y posteriores?** Absolutamente; la API está dirigida a Java 8+.

## ¿Qué es la compresión ccittfax3 java?

`CCITTFAX3` es un algoritmo de compresión monocromo sin pérdida diseñado para faxes e imágenes de documentos escaneados. Codifica cada píxel como un solo bit, ofreciendo una salida de alta calidad mientras reduce drásticamente el tamaño del archivo—a menudo entre un 70‑80 % comparado con TIFF sin comprimir. Esto lo hace ideal para archivar documentos en blanco y negro donde se debe preservar la fidelidad.

## ¿Por qué usar Aspose.Imaging para esta tarea?

Aspose.Imaging admite **100+** formatos de entrada y salida, incluidos PDF, PNG, JPEG y TIFF. Su arquitectura de transmisión puede manejar archivos TIFF de **cientos de páginas** sin cargar todo el documento en memoria, lo que lo hace ideal para proyectos de archivado a gran escala.

## Requisitos previos

- **Java Development Kit (JDK)** 8 o superior instalado.
- **IDE** como IntelliJ IDEA o Eclipse.
- **Maven** o **Gradle** para la gestión de dependencias.
- Conocimientos básicos de Java (clases, objetos, colecciones).

## Configuración de Aspose.Imaging para Java

Agregue la biblioteca a su archivo de compilación.

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

### Descarga directa

También puede descargar el JAR más reciente desde [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Obtención de licencia

Una licencia de prueba gratuita está disponible en [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Para uso en producción, compre una licencia permanente o solicite una temporal en [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Para un uso detallado de la API, consulte la [documentación](https://reference.aspose.com/imaging/java/) de Aspose.Imaging para Java.

### Inicialización básica

Después de agregar la dependencia, inicialice la biblioteca como se muestra a continuación.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## ¿Cómo configurar la compresión ccittfax3 java para un TIFF multipágina?

`TiffOptions` es una clase que define el formato de salida y la configuración de compresión para un archivo TIFF. Cargue el objeto `TiffOptions` con el enumerado `CCITTGroup3FaxCompression`, luego establezca la fuente del archivo de salida. Esta configuración de dos pasos prepara el escritor para compresión monocroma y garantiza que cada página añadida posteriormente se codifique usando el algoritmo CCITTFAX3, lo que resulta en una reducción significativa del tamaño mientras se preserva la calidad de la imagen.

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

## ¿Cómo crear una instancia de TiffImage en Java?

`TiffImage` representa un documento TIFF multipágina en memoria y proporciona métodos para manipular sus marcos. Primero, defina el ancho y alto que compartirán todas las páginas. Luego instancie `TiffImage` usando los `TiffOptions` creados previamente. El objeto `TiffImage` actúa como contenedor de los marcos individuales, permitiéndole agregar, eliminar o reordenar páginas antes de guardar el archivo final.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## ¿Cómo cargar y redimensionar imágenes de origen desde una carpeta?

Filtre el directorio objetivo en busca de archivos JPEG, lea cada imagen y redimensiónela para que coincida con el lienzo TIFF. Redimensionar antes de agregar marcos reduce el consumo de memoria y acelera la operación de guardado. Al convertir cada imagen de origen a las dimensiones y formato de píxel requeridos, garantiza una disposición de página coherente y evita errores en tiempo de ejecución cuando los marcos se añaden al documento TIFF.

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

## ¿Cómo agregar cada imagen como un marco al TIFF multipágina?

`TiffFrame` es un objeto que contiene una imagen de una sola página y sus metadatos asociados dentro de un TIFF. Itere sobre las imágenes redimensionadas, cree un nuevo `TiffFrame` y añádalo al `TiffImage`. Cada marco se convierte en una página separada en el documento final, y la biblioteca maneja automáticamente las actualizaciones de metadatos necesarias, como el recuento de páginas y los desplazamientos, garantizando una estructura TIFF multipágina válida.

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

## ¿Cómo guardar el archivo TIFF multipágina final?

Llame al método `save` en la instancia `TiffImage`, pasando la ruta de salida deseada. La biblioteca escribe automáticamente todos los marcos usando compresión CCITTFAX3, transmite los datos al disco de manera eficiente y cierra cualquier recurso subyacente. Después de que la operación de guardado se complete, el archivo resultante contiene todas las páginas con la compresión especificada, listo para distribución o archivado.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Aplicaciones prácticas

- **Archivado de documentos:** Almacene contratos, facturas o registros legales escaneados con una sobrecarga mínima de almacenamiento.  
- **Imágenes médicas:** Comprima escaneos de radiología mientras preserva el detalle diagnóstico.  
- **Producción de impresión:** Genere trabajos de impresión multipágina que las impresoras pueden consumir directamente.

## Consideraciones de rendimiento

- Utilice `ResizeOptions` que preserven la relación de aspecto para evitar distorsiones.  
- Cierre cada objeto `Image` después de agregar su marco para liberar memoria nativa.  
- Para lotes muy grandes, procese los archivos en flujos paralelos y escriba cada segmento TIFF de forma asíncrona.

## Problemas comunes y solución de problemas

- **Formato de píxel incorrecto:** CCITTFAX3 funciona solo con imágenes de 1 bit (blanco y negro). Convierta imágenes a color a escala de grises antes de redimensionar.  
- **Fugas de memoria:** Siempre llame a `dispose()` en objetos `Image` temporales; de lo contrario los búferes nativos permanecen asignados.  
- **El tamaño del archivo no se reduce:** Asegúrese de que la propiedad de compresión de `TiffOptions` esté configurada; de lo contrario se usa el valor predeterminado (sin compresión).

## Preguntas frecuentes

**P: ¿Puedo usar este enfoque con imágenes en color?**  
R: CCITTFAX3 está limitado a datos monocromos; para color use compresión JPEG o LZW en su lugar.

**P: ¿Aspose.Imaging admite transmisión para TIFF enormes?**  
R: Sí—la biblioteca escribe cada marco directamente al flujo de salida, manteniendo bajo el uso de memoria incluso para miles de páginas.

**P: ¿Cómo aplico una licencia temporal programáticamente?**  
R: Cargue el archivo `.lic` con `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**P: ¿Hay una forma de previsualizar el TIFF antes de guardarlo?**  
R: Puede renderizar cada `TiffFrame` a un `BufferedImage` y mostrarlo en un componente Swing.

**P: ¿Qué versiones de Java son oficialmente compatibles?**  
R: Aspose.Imaging admite Java 8 hasta Java 21, incluidas las versiones LTS.

## Conclusión

Ahora tiene un flujo de trabajo completo y listo para producción para crear archivos TIFF multipágina con **ccittfax3 compression java** usando Aspose.Imaging. Al seguir los pasos anteriores, puede archivar de manera eficiente colecciones masivas de documentos mientras mantiene bajos los costos de almacenamiento y alta la calidad de la imagen. Explore características adicionales de Aspose.Imaging—como OCR, manejo de metadatos y conversión de formatos—para mejorar aún más su canal de procesamiento de documentos.

---

**Última actualización:** 2026-09-28  
**Probado con:** Aspose.Imaging 25.5 for Java  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo crear TIFF multipágina con Aspose.Imaging para Java – Guía completa](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Cómo reducir el tamaño de archivo de imagen con compresión LZW en Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Dividir marcos TIFF multipágina con Aspose.Imaging para Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}