---
date: '2026-09-28'
description: Learn how to use ccittfax3 compression java to create multi-page TIFF
  files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for document
  workflows.
images:
- /java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/og-image.png
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Discover step‑by‑step how to use ccittfax3 compression java with Aspose.Imaging
  to build efficient multi‑page TIFF files for scanning and archiving.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: How to create multi-page TIFF with ccittfax3 compression java
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
title: How to create multi-page TIFF with ccittfax3 compression java
url: /java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mastering multi-page TIFF creation with ccittfax3 compression java using Aspose.Imaging

## Introduction

If you need to archive large volumes of scanned documents while keeping file sizes low, **ccittfax3 compression java** is the go‑to solution. This tutorial shows you how to generate multi‑page TIFF files with CCITTFAX3 compression in Java using Aspose.Imaging. You’ll learn why this compression works so well for monochrome scans, how to configure the library, and how to add each page as a frame.

**What you’ll learn**
- How to add Aspose.Imaging to a Java project.
- How to configure `TiffOptions` for CCITTFAX3 compression.
- How to create a `TiffImage`, resize source images, and add them as frames.
- How to save the final multi‑page TIFF efficiently.

Let’s walk through the complete implementation.

## Quick answers
- **What is the main benefit of CCITTFAX3 compression?** Up to 80 % reduction in file size for black‑and‑white scans.  
- **Which library provides built‑in support?** Aspose.Imaging for Java, version 25.5+.  
- **Do I need a license for development?** A free trial license works for all features; a paid license is required for production.  
- **Can I process hundreds of pages?** Yes—Aspose.Imaging streams pages, so memory usage stays low.  
- **Is the code compatible with Java 11 and later?** Absolutely; the API targets Java 8+.

## What is ccittfax3 compression java?
`CCITTFAX3` is a lossless, monochrome compression algorithm designed for fax and scanned document images. It encodes each pixel as a single bit, delivering high‑quality output while shrinking file size dramatically—often by 70‑80 % compared to uncompressed TIFF. This makes it ideal for archiving black‑and‑white documents where fidelity must be preserved.

## Why use Aspose.Imaging for this task?
Aspose.Imaging supports **100+** input and output formats, including PDF, PNG, JPEG, and TIFF. Its streaming architecture can handle **multi‑hundred‑page** TIFF files without loading the entire document into memory, making it ideal for large‑scale archiving projects.

## Prerequisites

- **Java Development Kit (JDK)** 8 or newer installed.
- **IDE** such as IntelliJ IDEA or Eclipse.
- **Maven** or **Gradle** for dependency management.
- Basic Java knowledge (classes, objects, collections).

## Setting up Aspose.Imaging for Java

Add the library to your build file.

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

### Direct download

You can also download the latest JAR from [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### License acquisition

A free trial license is available from [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). For production use, purchase a permanent license or request a temporary one at [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

For detailed API usage, see the Aspose.Imaging for Java [documentation](https://reference.aspose.com/imaging/java/).

### Basic initialization

After adding the dependency, initialise the library as shown below.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## How to configure ccittfax3 compression java for a multi‑page TIFF?

`TiffOptions` is a class that defines the output format and compression settings for a TIFF file. Load the `TiffOptions` object with the `CCITTGroup3FaxCompression` enum, then set the output file source. This two‑step configuration prepares the writer for monochrome compression and ensures that every page added later will be encoded using the CCITTFAX3 algorithm, resulting in significant size reduction while preserving image quality.

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

## How to create a TiffImage instance in Java?

`TiffImage` represents a multi‑page TIFF document in memory and provides methods to manipulate its frames. First, define the width and height that all pages will share. Then instantiate `TiffImage` using the previously created `TiffOptions`. The `TiffImage` object acts as a container for the individual frames, allowing you to add, remove, or reorder pages before saving the final file.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## How to load and resize source images from a folder?

Filter the target directory for JPEG files, read each image, and resize it to match the TIFF canvas. Resizing before adding frames reduces memory consumption and speeds up the save operation. By converting each source image to the required dimensions and pixel format, you guarantee consistent page layout and avoid runtime errors when the frames are appended to the TIFF document.

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

## How to add each image as a frame to the multi‑page TIFF?

`TiffFrame` is an object that holds a single page image and its associated metadata within a TIFF. Iterate over the resized images, create a new `TiffFrame`, and append it to the `TiffImage`. Each frame becomes a separate page in the final document, and the library automatically handles the necessary metadata updates, such as page count and offsets, ensuring a valid multi‑page TIFF structure.

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

## How to save the final multi‑page TIFF file?

Call the `save` method on the `TiffImage` instance, passing the desired output path. The library automatically writes all frames using CCITTFAX3 compression, streams the data to disk efficiently, and closes any underlying resources. After the save operation completes, the resulting file contains all pages with the specified compression, ready for distribution or archival.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Practical applications

- **Document archiving:** Store scanned contracts, invoices, or legal records with minimal storage overhead.  
- **Medical imaging:** Compress radiology scans while preserving diagnostic detail.  
- **Print production:** Generate multi‑page print jobs that printers can consume directly.

## Performance considerations

- Use `ResizeOptions` that preserve aspect ratio to avoid distortion.  
- Close each `Image` object after adding its frame to free native memory.  
- For very large batches, process files in parallel streams and write each TIFF segment asynchronously.

## Common pitfalls and troubleshooting

- **Incorrect pixel format:** CCITTFAX3 works only with 1‑bit (black‑and‑white) images. Convert color images to grayscale before resizing.  
- **Memory leaks:** Always call `dispose()` on temporary `Image` objects; otherwise native buffers remain allocated.  
- **File size not reduced:** Ensure the `TiffOptions` compression property is set; otherwise the default (no compression) is used.

## Frequently asked questions

**Q: Can I use this approach with color images?**  
A: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression instead.

**Q: Does Aspose.Imaging support streaming for huge TIFFs?**  
A: Yes—the library writes each frame directly to the output stream, keeping memory usage low even for thousands of pages.

**Q: How do I apply a temporary license programmatically?**  
A: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Is there a way to preview the TIFF before saving?**  
A: You can render each `TiffFrame` to a `BufferedImage` and display it in a Swing component.

**Q: Which Java versions are officially supported?**  
A: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.

## Conclusion

You now have a complete, production‑ready workflow for creating multi‑page TIFF files with **ccittfax3 compression java** using Aspose.Imaging. By following the steps above, you can efficiently archive massive document collections while keeping storage costs low and image quality high. Explore additional Aspose.Imaging features—such as OCR, metadata handling, and format conversion—to further enhance your document processing pipeline.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## Related Tutorials

- [How to Create Multi-Page TIFF with Aspose.Imaging for Java – A Complete Guide](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [How to Reduce Image File Size with LZW Compression in Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Split Multi Page TIFF Frames with Aspose.Imaging for Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}