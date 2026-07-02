---
date: 2026-02-12
description: Aprende cómo crear una imagen en blanco con Aspose y cómo dibujar un
  rectángulo en .NET con Aspose.Imaging – una guía rápida para la manipulación de
  imágenes en tus aplicaciones .NET.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Crear imagen en blanco con Aspose – Dibujar rectángulos en .NET
url: /es/net/basic-drawing/draw-rectangle/
weight: 14
---

Autor:**".

Now produce final content with all translations.

Check we didn't miss any text.

Also note "For Spanish, ensure proper RTL formatting if needed" not needed.

Make sure we keep all shortcodes and code block placeholders unchanged.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Crear Imagen en Blanco Aspose – Dibujar Rectángulos en .NET

Crear y manipular imágenes en aplicaciones .NET puede parecer intimidante, pero con Aspose.Imaging puedes **crear una imagen en blanco Aspose** en solo unas pocas líneas de código y luego dibujar formas en ella. En este tutorial recorreremos todo el proceso — desde configurar un lienzo en blanco hasta dibujar rectángulos—para que puedas comenzar a agregar gráficos a tus proyectos .NET de inmediato.

## Quick Answers
- **What does “create blank image Aspose” mean?** ¿Qué significa “create blank image Aspose”? Significa generar un bitmap vacío usando la API de Aspose.Imaging.  
- **How to draw rectangle .net with Aspose?** ¿Cómo dibujar un rectángulo en .NET con Aspose? Utiliza el método `Graphics.DrawRectangle` después de inicializar un objeto `Graphics`.  
- **Which NuGet package is required?** ¿Qué paquete NuGet se requiere? `Aspose.Imaging` (última versión).  
- **Can I save the image as PNG, JPEG, or BMP?** ¿Puedo guardar la imagen como PNG, JPEG o BMP? Sí – solo cambia las opciones de imagen (p.ej., `BmpOptions`, `JpegOptions`).  
- **Do I need a license for development?** ¿Necesito una licencia para desarrollo? Una prueba gratuita funciona para evaluación; se requiere una licencia comercial para producción.

## What is “create blank image Aspose”?
Crear una imagen en blanco significa asignar un búfer de píxeles con un ancho, alto y formato de píxel definidos. Aspose.Imaging maneja los detalles de bajo nivel, proporcionándote un lienzo listo para dibujar sin tener que trabajar con GDI+ o System.Drawing.

## Why use Aspose.Imaging for drawing rectangles in .NET?
- **Cross‑platform** – funciona en Windows, Linux y macOS.  
- **No native dependencies** – código puro administrado, perfecto para entornos de servidor.  
- **Rich drawing API** – admite lápices, pinceles, anti‑aliasing y muchos tipos de formas.  
- **High performance** – optimizado para imágenes grandes y procesamiento por lotes.

## Prerequisites

1. **Aspose.Imaging for .NET** – descárgalo desde la [página de descarga](https://releases.aspose.com/imaging/net/).  
2. **Development Environment** – Visual Studio, VS Code o cualquier IDE compatible con .NET.  
3. **.NET runtime** – .NET 6+ o .NET Framework 4.7.2+.  

Ahora que tenemos todo configurado, vamos a sumergirnos en el código.

## How to create a blank image Aspose in .NET?

### Step 1: Import the required namespaces

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Estos espacios de nombres te dan acceso a las clases principales de imaging, tipos de pinceles y opciones de guardado de imágenes.

### Step 2: Create a blank image (the canvas)

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

En este bloque:

* Definimos la ubicación de salida (`dataDir`).  
* Configuramos `BmpOptions` para usar un formato de píxel de 32 bits.  
* Creamos una **imagen en blanco** de 100 × 100 píxeles.  

### Step 3: How to draw rectangle .net with Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` rellena el lienzo con un color de fondo (amarillo en este ejemplo).  
* `DrawRectangle` dibuja dos rectángulos: uno con un lápiz rojo simple, otro con un pincel sólido azul, para contraste visual.

### Step 4: Save the image

```csharp
image.Save();
```

Llamar a `Save` escribe el bitmap en el sistema de archivos usando las opciones definidas anteriormente.

## Common Issues & Tips

| Problema | Razón | Solución |
|----------|-------|----------|
| **La imagen en blanco aparece negra** | Fondo no limpiado | Llama a `graphic.Clear(Color.YourColor)` antes de dibujar. |
| **Excepción de archivo no encontrado** | `dataDir` apunta a una carpeta que no existe | Asegúrate de que el directorio exista o usa `Path.Combine` con `Environment.CurrentDirectory`. |
| **Colores incorrectos** | Usando `System.Drawing.Color` en lugar de `Aspose.Imaging.Color` | Siempre importa `Aspose.Imaging.Color`. |
| **Retardo de rendimiento en imágenes grandes** | Usando `BmpOptions` predeterminado con alto bits‑por‑píxel | Cambia a `JpegOptions` o `PngOptions` para compresión. |

## Frequently Asked Questions (Extended)

**Q: ¿Puedo dibujar otras formas además de rectángulos?**  
A: Por supuesto. Aspose.Imaging proporciona métodos como `DrawEllipse`, `DrawLine` y `DrawPolygon`.

**Q: ¿La biblioteca es gratuita para uso comercial?**  
A: No, Aspose.Imaging es un producto comercial, pero puedes evaluarlo con una prueba gratuita disponible [aquí](https://releases.aspose.com/).

**Q: ¿Esto funciona tanto en Windows como en aplicaciones web?**  
A: Sí, el mismo código se ejecuta en ASP.NET, Blazor y aplicaciones de consola.

**Q: ¿Cómo cambio el formato de salida a PNG?**  
A: Reemplaza `BmpOptions` con `PngOptions` y ajusta la extensión del archivo en consecuencia.

**Q: ¿Dónde puedo encontrar documentación más detallada?**  
A: Accede a la referencia completa de la API [aquí](https://reference.aspose.com/imaging/net/) y únete a la comunidad en el [foro de Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-02-12  
**Probado con:** Aspose.Imaging 24.12 for .NET  
**Autor:** Aspose