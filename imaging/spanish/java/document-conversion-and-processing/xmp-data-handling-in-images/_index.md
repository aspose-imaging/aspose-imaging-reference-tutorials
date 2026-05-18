---
date: 2026-05-18
description: Aprenda cómo usar la biblioteca de procesamiento de imágenes Java Aspose.Imaging
  para incrustar y recuperar metadatos XMP en imágenes, con código paso a paso.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: Manejo de datos XMP en imágenes
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Biblioteca de procesamiento de imágenes Java: XMP con Aspose.Imaging'
url: /es/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Manipulación de datos XMP en imágenes con Aspose.Imaging para Java

Aspose.Imaging es una **biblioteca de procesamiento de imágenes java** que le permite trabajar con docenas de formatos raster y vectoriales. En este tutorial aprenderá cómo incrustar y recuperar datos XMP (Extensible Metadata Platform) en imágenes usando Aspose.Imaging para Java. Al final, podrá almacenar autor, descripción y metadatos personalizados directamente dentro de sus archivos de imagen, haciéndolos buscables y auto‑descriptivos.

## Respuestas rápidas
- **¿Qué es XMP?** XMP es un formato estandarizado basado en XML para incrustar metadatos dentro de archivos como imágenes, PDFs y videos.  
- **¿Qué biblioteca maneja XMP en Java?** Aspose.Imaging para Java proporciona una API completa para leer y escribir paquetes XMP.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Cuántos formatos de imagen son compatibles?** Más de 150 formatos, incluidos TIFF, JPEG, PNG, PSD y RAW.  
- **¿Puedo procesar imágenes grandes?** Sí – la biblioteca puede manejar archivos de hasta 2 GB sin cargar la imagen completa en memoria.

## ¿Qué son los metadatos XMP?
Los metadatos XMP son un estándar basado en XML que incrusta información descriptiva directamente en archivos digitales. Permite el almacenamiento coherente de autor, derechos de autor, palabras clave y datos personalizados entre aplicaciones. Como es XML, XMP puede extenderse con espacios de nombres personalizados, lo que permite a los desarrolladores agregar campos propietarios mientras siguen siendo compatibles con herramientas que entienden el esquema central. Esto hace que XMP sea ideal para la gestión de activos a largo plazo y la interoperabilidad entre aplicaciones.

## ¿Por qué usar una biblioteca de procesamiento de imágenes Java para XMP?
Aspose.Imaging para Java soporta **más de 150 formatos de imagen** y puede procesar archivos de varios gigabytes de forma streaming, reduciendo el consumo de memoria hasta en un 80 % comparado con la carga ingenua. La API también garantiza que los paquetes XMP cumplan con los estándares, asegurando la compatibilidad con Adobe Photoshop, Lightroom y otras herramientas.

## Requisitos previos

Antes de comenzar, asegúrese de tener los siguientes requisitos:

- Un entorno de desarrollo Java configurado en su computadora.  
- Biblioteca Aspose.Imaging para Java instalada. Puede descargarla desde el [sitio web de Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/).  
- Un conocimiento básico de programación Java.

## Importación de paquetes

Comience importando los paquetes necesarios a su proyecto Java. Puede añadir las siguientes sentencias de importación al inicio de su código:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Ahora, desglosaremos el ejemplo paso a paso:

## ¿Cómo incrustar metadatos XMP usando una biblioteca de procesamiento de imágenes Java?

Cargue su imagen, cree un paquete XMP, adjunte el paquete a la imagen y guarde – todo en unas pocas líneas concisas. El método `setXmpData` de Aspose.Imaging escribe el paquete directamente en el archivo sin requerir un archivo de metadatos separado. El proceso funciona tanto con imágenes basadas en archivos como en flujos, lo que lo hace adecuado para servicios web y trabajos por lotes.

### Paso 1: Especificar el tamaño de la imagen y opciones TIFF

Primero, defina el directorio donde se almacenará su imagen y cree un `Rectangle` para especificar el tamaño de la imagen. En este ejemplo, usamos una imagen TIFF con ciertas opciones. `TiffOptions` configura ajustes específicos del formato para la imagen TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Paso 2: Crear una nueva imagen

Ahora, cree una nueva imagen con las opciones especificadas. Esta imagen se utilizará para almacenar los metadatos XMP. `TiffImage` representa un objeto de imagen TIFF, y `TiffFrame` define un marco individual dentro de ella.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Paso 3: Crear encabezado y remolque XMP

Cree instancias de XMP‑Header y XMP‑Trailer para sus metadatos XMP. Estos encabezados y remolques ayudan a definir la estructura de los metadatos. `XmpHeaderPi` y `XmpTrailerPi` representan las secciones de apertura y cierre del paquete XMP.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Paso 4: Crear información meta XMP

Ahora, cree una instancia de meta XMP para establecer diferentes atributos. Puede agregar información como el autor y la descripción. `XmpMeta` contiene los campos principales de metadatos como autor y descripción.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Paso 5: Crear contenedor de paquete XMP

`XmpPacketWrapper` es el contenedor que mantiene el encabezado XMP, el remolque y la información meta en un solo paquete. Garantiza que el paquete cumpla con la especificación XMP. `XmpPacketWrapper` empaqueta el encabezado, la meta y el remolque en un único paquete XMP.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Paso 6: Añadir paquete Photoshop

Para almacenar información específica de Photoshop, cree un paquete Photoshop y establezca sus atributos, como ciudad, país y modo de color. Luego, añada este paquete a los metadatos XMP. `PhotoshopPackage` almacena metadatos específicos de Photoshop como ciudad, país y modo de color.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Paso 7: Añadir paquete Dublin Core

Para información más general, como autor, título y valores adicionales, cree un paquete DublinCore y establezca sus atributos. Añada también este paquete a los metadatos XMP. `DublinCorePackage` contiene campos estándar de Dublin Core como título, creador y palabras clave.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Paso 8: Actualizar metadatos XMP en la imagen

Actualice los metadatos XMP en la imagen usando el método `setXmpData`. Esta llamada escribe el paquete XMP en la sección de metadatos de la imagen. `setXmpData` escribe el paquete XMP en la sección de metadatos de la imagen.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Paso 9: Guardar la imagen

Ahora puede guardar la imagen con los metadatos XMP incrustados en el disco o en un flujo de memoria.

```java
    image.save(ms);
```

### Paso 10: Cargar la imagen y recuperar metadatos XMP

Para recuperar los metadatos XMP de la imagen, cargue la imagen desde el flujo de memoria o el disco y acceda a los datos XMP mediante el método `getXmpData`. `getXmpData` lee el paquete XMP incrustado de la imagen.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

¡Felicidades! Ha aprendido con éxito cómo manejar datos XMP en imágenes usando Aspose.Imaging para Java. Esto le permite almacenar y recuperar valiosos metadatos dentro de sus archivos de imagen.

## Problemas comunes y soluciones

- **Los metadatos no aparecen en Photoshop:** Asegúrese de que el paquete XMP siga el esquema XML adecuado; Aspose.Imaging lo valida automáticamente, pero los espacios de nombres personalizados pueden necesitar registro.  
- **Archivos TIFF grandes provocan OutOfMemoryError:** Use `TiffOptions` con `Compression` configurado a `LZW` y habilite streaming (`loadOptions.setBufferSize`) para mantener bajo el uso de memoria.  
- **Codificación de caracteres inesperada:** XMP espera UTF‑8; siempre pase cadenas usando `StandardCharsets.UTF_8` para evitar datos corruptos.

## Preguntas frecuentes

**P: ¿Qué son los metadatos XMP?**  
R: XMP es un estándar basado en XML para incrustar información descriptiva directamente dentro de archivos, permitiendo metadatos consistentes entre aplicaciones.

**P: ¿Por qué son importantes los metadatos XMP?**  
R: Le permite etiquetar imágenes con autor, derechos de autor, palabras clave y datos personalizados, mejorando la capacidad de búsqueda y la gestión de activos sin bases de datos externas.

**P: ¿Puedo editar los metadatos XMP después de incrustarlos en una imagen?**  
R: Sí, Aspose.Imaging para Java proporciona métodos para modificar paquetes XMP existentes y volver a escribirlos en el archivo.

**P: ¿Aspose.Imaging para Java es una herramienta gratuita?**  
R: Hay una prueba gratuita disponible para evaluación, pero se requiere una licencia de pago para uso en producción. Puede explorar opciones en el [sitio web de Aspose.Imaging para Java](https://purchase.aspose.com/buy).

**P: ¿Dónde puedo obtener ayuda y soporte para Aspose.Imaging para Java?**  
R: Visite los [foros de Aspose.Imaging](https://forum.aspose.com/) para asistencia de la comunidad, o contacte directamente al soporte de Aspose para clientes con licencia de pago.

## Conclusión

En este tutorial, exploramos cómo trabajar con metadatos XMP en imágenes usando Aspose.Imaging para Java, una **biblioteca de procesamiento de imágenes java** líder. Siguiendo la guía paso a paso, puede incrustar, actualizar y recuperar fácilmente datos XMP, enriqueciendo sus activos digitales con metadatos buscables y compatibles con estándares.

---

**Última actualización:** 2026-05-18  
**Probado con:** Aspose.Imaging para Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Domine el procesamiento de imágenes Java: Modifique datos EXIF con Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Procesamiento de imágenes Java con Aspose.Imaging: Cargar, mejorar y guardar imágenes](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Procesamiento avanzado de imágenes Java con la biblioteca Aspose.Imaging](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```