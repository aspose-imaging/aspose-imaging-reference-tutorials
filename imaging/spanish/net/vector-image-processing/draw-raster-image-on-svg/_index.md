---
"description": "Aprenda a dibujar imágenes rasterizadas en SVG con Aspose.Imaging para .NET. Mejore sus aplicaciones .NET con imágenes dinámicas."
"linktitle": "Dibujar una imagen rasterizada en SVG en Aspose.Imaging para .NET"
"second_title": "API de procesamiento de imágenes Aspose.Imaging .NET"
"title": "Cómo dibujar una imagen rasterizada en SVG en Aspose.Imaging para .NET"
"url": "/es/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cómo dibujar una imagen rasterizada en SVG en Aspose.Imaging para .NET


En el mundo de la programación .NET, Aspose.Imaging se destaca como una biblioteca confiable y versátil para gestionar diversas tareas relacionadas con imágenes. Una de sus fascinantes funciones es la de dibujar una imagen rasterizada en un lienzo SVG. En esta guía paso a paso, le guiaremos a través del proceso de dibujar una imagen rasterizada en un SVG usando Aspose.Imaging para .NET.

## Prerrequisitos

Antes de profundizar en los detalles, asegúrese de tener los siguientes requisitos previos:

- Aspose.Imaging para .NET: Debe tener la biblioteca instalada. De lo contrario, puede descargarla desde [Página de descarga de Aspose.Imaging para .NET](https://releases.aspose.com/imaging/net/).

- Su directorio de documentos: Reemplazar `"Your Document Directory"` con la ruta real a su directorio de trabajo.

Ahora, desglosemos el proceso en pasos fáciles de seguir:

## Paso 1: Importar los espacios de nombres necesarios

Debe importar los espacios de nombres necesarios para trabajar con Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Paso 2: Cargar las imágenes

- Primero, cargue la imagen rasterizada que desea dibujar en el lienzo SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- A continuación, cargue la imagen de lienzo SVG donde desea dibujar la imagen rasterizada.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Paso 3: Dibujar en la imagen SVG

Ahora puedes empezar a dibujar en la imagen SVG existente. Para ello, necesitas crear una instancia de `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Paso 4: Dibuja la imagen rasterizada

- Define los límites donde quieres dibujar la imagen rasterizada y especifica la región de origen de la imagen rasterizada.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Paso 5: Guardar el resultado

Después de dibujar la imagen rasterizada en el lienzo SVG, puedes guardar la imagen resultante:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusión

¡Felicitaciones! Has dibujado con éxito una imagen rasterizada en un lienzo SVG con Aspose.Imaging para .NET. Esto puede ser increíblemente útil para crear imágenes ricas y dinámicas en tus aplicaciones .NET.

Para obtener más información y documentación detallada, visite el sitio web [Documentación de Aspose.Imaging para .NET](https://reference.aspose.com/imaging/net/).

## Preguntas frecuentes

### ¿Qué es Aspose.Imaging para .NET?
   Aspose.Imaging para .NET es una poderosa biblioteca de procesamiento de imágenes que permite a los desarrolladores crear, manipular y convertir imágenes en varios formatos dentro de aplicaciones .NET.

### ¿Puedo utilizar Aspose.Imaging for .NET en proyectos comerciales?
   Sí, puede usar Aspose.Imaging para .NET tanto en proyectos comerciales como no comerciales. Puede encontrar información sobre la licencia en [página de compra](https://purchase.aspose.com/buy).

### ¿Hay una prueba gratuita disponible?
   Sí, puede obtener una prueba gratuita de Aspose.Imaging para .NET desde [aquí](https://releases.aspose.com/).

### ¿Dónde puedo obtener ayuda o hacer preguntas?
   Si tienes alguna pregunta o necesitas ayuda, puedes visitar el [Foro de Aspose.Imaging](https://forum.aspose.com/).

### ¿Cómo puedo obtener una licencia temporal para Aspose.Imaging para .NET?
   Puede obtener una licencia temporal de [aquí](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}