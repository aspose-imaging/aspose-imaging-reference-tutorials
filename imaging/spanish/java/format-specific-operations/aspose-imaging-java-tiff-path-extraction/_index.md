---
date: '2026-09-02'
description: Aprenda cómo crear una ruta de recorte y extraerla de imágenes TIFF usando
  Aspose.Imaging for Java. Siga instrucciones paso a paso para convertir TIFF a PSD
  de manera eficiente.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Aprenda cómo crear una ruta de recorte y extraerla de imágenes TIFF
  usando Aspose.Imaging for Java. Siga código paso a paso para convertir TIFF a PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Crear ruta de recorte en TIFF con Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Crear ruta de recorte en TIFF con Aspose.Imaging for Java
url: /es/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear ruta de recorte en TIFF con Aspose.Imaging para Java

En esta guía completa aprenderás **cómo crear una ruta de recorte** en un archivo TIFF y cómo extraer rutas existentes usando Aspose.Imaging para Java. Al final, podrás convertir imágenes TIFF en archivos PSD totalmente editables, listos para Photoshop o cualquier editor que admita vectores.

## Respuestas rápidas
- **¿Qué es una ruta de recorte?** Un contorno vectorial que define regiones transparentes y opacas de una imagen.  
- **¿Puedo extraer una ruta existente de un TIFF?** Sí – Aspose.Imaging puede leer recursos de ruta incrustados y guardarlos como PSD.  
- **¿Cómo añado una nueva ruta de recorte?** Crea un `PathResource`, pópúlalo con registros vectoriales y asígnalo al marco activo de la imagen.  
- **¿Necesito una licencia para uso en producción?** Se requiere una licencia válida de Aspose.Imaging para implementaciones comerciales.  
- **¿Qué versión de Java se necesita?** JDK 8 o superior; la biblioteca funciona con Java 11, 17 y versiones posteriores.

## ¿Qué es una ruta de recorte?
Una ruta de recorte es un contorno basado en vectores que indica a los motores de renderizado qué partes de una imagen mostrar u ocultar. Se almacena como un recurso de ruta dentro de archivos TIFF o PSD y puede editarse en Adobe Photoshop.

## ¿Por qué convertir TIFF a PSD?
Convertir TIFF a PSD permite la edición sin pérdida de capas, máscaras y rutas de recorte. Aspose.Imaging admite **más de 50 formatos de entrada y salida** y puede procesar TIFFs de cientos de páginas sin cargar todo el archivo en memoria, ofreciendo una conversión por lotes de alto rendimiento.

## Requisitos previos
- **Java Development Kit (JDK)** 8 o más reciente instalado.
- Biblioteca **Aspose.Imaging para Java** (añadir vía Maven, Gradle o descarga directa).  
- Familiaridad básica con conceptos de programación en Java.

## Cómo configurar Aspose.Imaging para Java
Antes de añadir código, asegúrate de que la biblioteca está referenciada correctamente en tu sistema de compilación y de que dispones de un archivo de licencia válido. Esto garantiza que la API funcione sin restricciones de evaluación y que todas las funciones, incluida la manipulación de rutas, estén disponibles.

### Maven
Agrega la siguiente dependencia a tu archivo `pom.xml`:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Incluye esta línea en tu archivo `build.gradle`:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Descarga directa
Descarga la última versión desde [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Obtención de licencia
1. **Prueba gratuita** – comienza con una prueba de 30 días.  
2. **Licencia temporal** – obtén una en la [temporary license page](https://purchase.aspose.com/temporary-license/).  
3. **Compra** – adquiere una licencia completa en el [Aspose's website](https://purchase.aspose.com/buy).

Una vez instalado y con licencia, inicializa Aspose.Imaging en tu proyecto:
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## ¿Cómo extraer la ruta de recorte de un TIFF?
Extraer una ruta de recorte implica cargar el TIFF, localizar los recursos de ruta incrustados y escribir esos recursos en un nuevo archivo PSD. El proceso lee los datos vectoriales directamente de la imagen fuente, preservando la precisión y evitando la conversión a raster.

Carga el TIFF, itera a través de sus recursos de ruta y guarda el resultado como un PSD. Esta operación lee los datos vectoriales incrustados y los escribe en un nuevo archivo en una sola pasada.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Itera a través de los recursos de ruta en el marco activo y recógelos:
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Guarda la imagen con las rutas extraídas en un nuevo archivo PSD:
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## ¿Cómo crear una ruta de recorte en TIFF?
Crear una ruta de recorte requiere construir un `PathResource` que describa el contorno vectorial deseado, adjuntarlo al marco activo del TIFF y luego guardar la imagen (o una copia) como PSD para que la ruta se conserve. Este enfoque permite añadir máscaras vectoriales a archivos raster de forma programática.

`PathResource` representa una ruta vectorial almacenada dentro de un archivo de imagen.  
Inicializa un nuevo `PathResource` con los atributos requeridos:
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Asigna el recurso de ruta creado al marco activo de la imagen:
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Guarda el TIFF modificado como un PSD que ahora contiene la ruta de recorte:
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Métodos auxiliares

### Crear registros
Genera registros de ruta vectorial usando nudos Bezier y registros de longitud:
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Crear registros Bezier
Convierte matrices de coordenadas en registros de ruta vectorial Bezier:
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Crear registro Bezier
Define un único registro de ruta vectorial Bezier:
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Aplicaciones prácticas
1. **Flujos de trabajo de diseño gráfico** – Convierte TIFF a PSD para editar capas y máscaras en Photoshop.  
2. **Pipelines de imágenes automatizados** – Procesa por lotes miles de TIFFs, extrayendo o añadiendo rutas al vuelo.  
3. **Visualizaciones basadas en datos** – Usa rutas vectoriales para generar gráficos o esquemas precisos a partir de fuentes raster.

## Consideraciones de rendimiento
- **Gestión de memoria** – Utiliza try‑with‑resources para asegurar que los objetos de imagen se liberen rápidamente.  
- **Procesamiento por lotes** – Paraleliza conversiones con `ForkJoinPool` de Java para conjuntos de imágenes grandes.  
- **Manejo de resolución** – Ajusta DPI solo cuando sea necesario para mantener bajo el tiempo de procesamiento sin sacrificar calidad.

## Conclusión
Ahora sabes **cómo crear una ruta de recorte** en archivos TIFF y extraer rutas existentes usando Aspose.Imaging para Java. Estas técnicas te permiten integrar una manipulación de imágenes sofisticada en cualquier flujo de trabajo basado en Java, desde utilidades de escritorio hasta pipelines de procesamiento a nivel empresarial.

### Próximos pasos
- Experimenta con diferentes formas vectoriales y atributos de ruta.  
- Explora funciones adicionales de Aspose.Imaging como marcas de agua, conversión de formatos y manejo de metadatos.

## Preguntas frecuentes

**Q: ¿Puedo usar Aspose.Imaging para Java en una aplicación comercial?**  
A: Sí, siempre que dispongas de una licencia comercial válida; hay una prueba gratuita disponible para evaluación.

**Q: ¿Qué formatos de imagen admite Aspose.Imaging?**  
A: La biblioteca admite más de 100 formatos, incluidos TIFF, PSD, BMP, JPEG, PNG y muchos más.

**Q: ¿Cómo soluciono errores de extracción de rutas?**  
A: Verifica que el TIFF de origen realmente contenga recursos de ruta vectorial; usa la comprobación `hasPathResources()` antes de la extracción.

**Q: ¿Es posible el procesamiento por lotes de varios TIFF?**  
A: Absolutamente – combina el código de extracción con streams paralelos de Java o un executor service para manejar muchos archivos de forma eficiente.

**Q: ¿Existen limitaciones al crear rutas de recorte en TIFF?**  
A: Las formas complejas pueden requerir ajuste manual después de la creación; la API maneja de forma fiable curvas Bezier estándar y líneas rectas.

**Last Updated:** 2026-09-02  
**Tested With:** Aspose.Imaging for Java 24.12  
**Author:** Aspose  

## Recursos

- [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)
- [Download Aspose.Imaging for Java](https://releases.aspose.com/imaging/java/)
- [Purchase License](https://purchase.aspose.com/buy)
- [Free Trial](https://releases.aspose.com/imaging/java/)
- [Temporary License](https://purchase.aspose.com/temporary-license/)
- [Aspose Support Forum](https://forum.aspose.com/c/imaging/14)

## Tutoriales relacionados

- [Convert Image to PSD with Aspose.Imaging for Java – Step‑by‑Step Guide](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [How to Convert TIFF to GraphicsPath with Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Efficiently Load & Save TIFF Images in Java with Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}