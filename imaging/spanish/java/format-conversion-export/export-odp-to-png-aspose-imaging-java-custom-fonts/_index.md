---
date: '2026-06-28'
description: Aprenda cómo convertir ODP a PNG usando Aspose.Imaging for Java, configure
  fuentes personalizadas y desactive las fuentes del sistema para una renderización
  precisa.
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
title: Cómo convertir ODP a PNG con Aspose.Imaging for Java – Guía de fuentes personalizadas
  y exportación
url: /es/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Cómo convertir ODP a PNG con Aspose.Imaging para Java – Fuentes personalizadas y guía de exportación

En las aplicaciones Java modernas, convertir archivos OpenDocument Presentation (ODP) a imágenes PNG de alta calidad es un requisito común, especialmente cuando necesita preservar la identidad de marca mediante fuentes personalizadas. Este tutorial muestra **cómo convertir ODP** a PNG usando Aspose.Imaging para Java, le guía a través de la configuración de una carpeta de fuentes personalizada, la desactivación de fuentes de respaldo del sistema y el ajuste fino de las opciones de rasterización para un rendimiento óptimo.

**What You’ll Learn**
- Cómo establecer un directorio de fuentes personalizado para la conversión de ODP.  
- Cómo desactivar las fuentes alternativas del sistema para que solo se usen sus tipografías elegidas.  
- Cómo exportar un archivo ODP a PNG con dimensiones precisas y configuraciones de fuentes.  
- Consejos para mejorar la velocidad y el uso de memoria al procesar presentaciones grandes.

## Respuestas rápidas
- **¿Puedo usar Maven para agregar Aspose.Imaging?** Sí, agregue la dependencia Maven y ejecute `mvn install`.  
- **¿Necesito una licencia para producción?** Se requiere una licencia válida de Aspose.Imaging para uso ilimitado.  
- **¿Se respetarán mis fuentes personalizadas?** Configure la carpeta de fuentes y desactive las alternativas del sistema para aplicarlas.  
- **¿Qué formatos de imagen son compatibles?** Aspose.Imaging admite más de 120 formatos raster y vectoriales, incluidos PNG, JPEG, TIFF y WebP.  
- **¿Es la API segura para subprocesos?** Sí, la mayoría de las clases de Aspose.Imaging son seguras para uso concurrente cuando crea instancias separadas por subproceso.

## Qué es “how to convert odp”?
*“How to convert odp”* se refiere al proceso de transformar un archivo OpenDocument Presentation a otro formato—comúnmente PNG—mientras se preserva el diseño, las fuentes y la fidelidad visual. Aspose.Imaging para Java ofrece un flujo de trabajo de un solo método que maneja esta conversión sin requerir herramientas externas, permitiendo a los desarrolladores integrar la conversión directamente en sus aplicaciones con código mínimo.

## ¿Por qué usar Aspose.Imaging para Java?
Aspose.Imaging admite **más de 120 formatos de salida** y puede rasterizar archivos ODP de varias páginas sin cargar todo el documento en memoria, reduciendo el uso máximo de RAM hasta en un 70 % en presentaciones grandes. La biblioteca también ofrece gestión de fuentes incorporada, eliminando la necesidad de motores de renderizado de terceros.

## Requisitos previos
- **Bibliotecas**: Aspose.Imaging para Java ≥ 25.5.  
- **JDK**: Versión 8 o superior.  
- **IDE**: IntelliJ IDEA, Eclipse o cualquier editor compatible con Java.  
- **Conocimientos básicos**: Java I/O, programación orientada a objetos y conceptos de imágenes.

## Instrucciones de instalación

### Maven
Agregue la siguiente dependencia a su `pom.xml` y ejecute `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Incluya la biblioteca en su archivo `build.gradle` y actualice el proyecto:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Descarga directa
Descargue el JAR más reciente desde [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Pasos para adquirir licencia
Para desbloquear la funcionalidad completa, aplique una licencia temporal o permanente:

1. **Prueba gratuita** – No se requiere licencia, funciones limitadas.  
2. **Licencia temporal** – Solicite una en el [sitio web de Aspose](https://purchase.aspose.com/temporary-license/).  
3. **Compra** – Adquiera una suscripción o licencia perpetua desde la [página de compra de Aspose](https://purchase.aspose.com/buy).

Inicialice la biblioteca con su archivo de licencia:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## ¿Cómo establecer un directorio de fuentes personalizado para la conversión de ODP?
`FontSettings` es una clase que gestiona los recursos de fuentes para Aspose.Imaging. Cargue sus fuentes personalizadas antes de que comience cualquier procesamiento de imágenes. Esto garantiza que cada diapositiva use exactamente las tipografías que usted proporciona.

Establezca la ruta de la carpeta de fuentes usando `FontSettings` de Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Ancla de definición*: `FontSettings.setFontsFolder` indica a Aspose.Imaging dónde buscar fuentes TrueType y OpenType en el sistema de archivos.

## ¿Cómo desactivar las fuentes alternativas del sistema durante la conversión de ODP?
Desactivar las alternativas del sistema obliga al motor de renderizado a ignorar las fuentes instaladas en el sistema operativo, garantizando que solo se usen las fuentes que usted proporciona. Esto elimina sustituciones de fuentes inesperadas que pueden alterar la apariencia visual de sus diapositivas.

Desactive las alternativas del sistema con la siguiente llamada:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Ancla de definición*: `FontSettings.setGetSystemAlternativeFont(false)` obliga al motor a usar solo las fuentes ubicadas en la carpeta que definió, eliminando sustituciones inesperadas.

## ¿Cómo exportar un archivo ODP a PNG con una fuente especificada?
`RasterizationOptions` define cómo se rasterizan las páginas vectoriales en imágenes bitmap. Al combinar la configuración de fuentes con los ajustes de rasterización, puede controlar DPI, color de fondo y tamaño de página para cada PNG exportado.

Implemente el método de exportación como se muestra a continuación:

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

*Ancla de definición*: La clase `RasterizationOptions` controla DPI, tamaño de página y color de fondo para los archivos PNG generados.

### Problemas comunes y soluciones
- **Archivos de fuente faltantes** – Verifique que cada `.ttf` u `.otf` referenciado en el ODP esté presente en la carpeta que configuró.  
- **Rutas de archivo incorrectas** – Use rutas absolutas o resuelva rutas relativas contra `System.getProperty("user.dir")`.  
- **Permisos insuficientes** – Asegúrese de que el proceso Java pueda leer la carpeta de fuentes y escribir en la carpeta de salida.

## Aplicaciones prácticas
1. **Presentaciones coherentes con la marca** – Exporte presentaciones como PNG para publicación web mientras preserva las fuentes corporativas.  
2. **Generación automática de informes** – Convierta cada diapositiva en una imagen para incluirla en informes PDF o boletines de correo electrónico.  
3. **Creación de archivo legado** – Almacene contenido ODP como PNG para garantizar la accesibilidad futura sin necesidad de visores ODP.

## Consideraciones de rendimiento
- Utilice la última versión de Aspose.Imaging para beneficiarse de mejoras de rasterización multihilo (hasta 2× más rápido en CPU de 8 núcleos).  
- Envuelva el procesamiento de imágenes en un bloque try‑with‑resources para garantizar la eliminación oportuna de recursos nativos.  
- Ajuste `RasterizationOptions` (p. ej., DPI más bajo) al procesar miles de diapositivas para equilibrar calidad y uso de memoria.

## Preguntas frecuentes

**P: ¿Cuál es la versión mínima de Java requerida?**  
R: Aspose.Imaging para Java funciona con JDK 8 y versiones posteriores; se recomienda JDK 11 para soporte a largo plazo.

**P: ¿Puedo convertir solo diapositivas seleccionadas?**  
R: Sí, establezca `rasterizationOptions.setPageNumber(specificSlideIndex)` antes de llamar a `save`.

**P: ¿Cómo manejo archivos ODP protegidos con contraseña?**  
R: Cargue el archivo con `LoadOptions` que incluya la contraseña, luego continúe con la misma configuración de fuentes.

**P: ¿Desactivar las fuentes del sistema afecta el rendimiento?**  
R: Mejora ligeramente la velocidad porque el motor omite la búsqueda de fuentes del sistema, especialmente perceptible en máquinas con grandes colecciones de fuentes.

**P: ¿Dónde puedo encontrar más ejemplos de código?**  
R: Explore la [documentación oficial de Aspose.Imaging](https://reference.aspose.com/imaging/java/) para escenarios adicionales como conversión por lotes y transformaciones de imágenes.

## Recursos adicionales
- [Lanzamientos de Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/)  
- [Lanzamientos de Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [Comience su prueba gratuita](https://releases.aspose.com/imaging/java/)  
- [Documentación de Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Foro de Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Comprar licencia de Aspose](https://purchase.aspose.com/buy)  
- [Solicitar una licencia temporal](https://purchase.aspose.com/temporary-license/)  

---

**Última actualización:** 2026-06-28  
**Probado con:** Aspose.Imaging for Java 25.5  
**Autor:** Aspose

## Tutoriales relacionados

- [Convertir ODG a PNG con Aspose.Imaging para Java: Guía completa](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Conversión eficiente de imágenes en Java con Aspose.Imaging: Guía completa](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}