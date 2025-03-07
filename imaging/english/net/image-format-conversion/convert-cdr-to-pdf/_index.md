---
title: Converting CDR to PDF with Aspose.Imaging for .NET
linktitle: Convert CDR to PDF in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Learn how to convert CDR to PDF in Aspose.Imaging for .NET. A step-by-step guide for seamless conversions.
weight: 10
url: /net/image-format-conversion/convert-cdr-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converting CDR to PDF with Aspose.Imaging for .NET

In the world of graphic design and document processing, the need to convert CorelDRAW (CDR) files to PDF format is a common occurrence. Aspose.Imaging for .NET offers a powerful solution for achieving this conversion seamlessly. In this tutorial, we will guide you through the process of converting CDR files to PDF using Aspose.Imaging for .NET. We'll break down each step, providing clear explanations and code examples to make the process easy to follow.

## Prerequisites

Before we dive into the conversion process, there are a few prerequisites you should have in place:

1. Aspose.Imaging for .NET: Make sure you have Aspose.Imaging for .NET installed in your development environment. You can download it from the [website](https://releases.aspose.com/imaging/net/).

2. A CDR File: You'll need a CorelDRAW (CDR) file that you want to convert to PDF.

3. Development Environment: Have a suitable development environment set up with Visual Studio or any other .NET development tool.

Now, let's begin the step-by-step guide.

## Step 1: Import Namespaces

The first step is to import the necessary namespaces from Aspose.Imaging. These namespaces will provide the classes and methods needed for the conversion process.

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Cdr;
using Aspose.Imaging.FileFormats.Pdf;
using Aspose.Imaging.ImageOptions;
```

## Step 2: Load the CDR File

To start the conversion process, you need to load the CDR file. Here's how you can do it:

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "YourFile.cdr";

using (var image = (VectorMultipageImage)Image.Load(inputFileName))
{
    // Your code will go here.
}
```

## Step 3: Create Page Rasterization Options

In this step, we'll create page rasterization options for each page in the CDR image. These options determine how the pages will be converted.

```csharp
var pageOptions = CreatePageOptions<CdrRasterizationOptions>(image);
```

## Step 4: Set Page Size

For each page, you'll need to set the page size for rasterization.

```csharp
private static VectorRasterizationOptions CreatePageOptions<TOptions>(Size pageSize) where TOptions : VectorRasterizationOptions
{
    var options = Activator.CreateInstance<TOptions>();
    options.PageSize = pageSize;
    return options;
}
```

## Step 5: Create PDF Options

Now, create the PDF options, including the page rasterization options you've defined.

```csharp
var options = new PdfOptions { MultiPageOptions = new MultiPageOptions { PageRasterizationOptions = pageOptions } };
```

## Step 6: Export to PDF

Finally, export the CDR image to PDF format with the options you've configured.

```csharp
image.Save(dataDir + "YourFile.cdr.pdf", options);
```

## Step 7: Clean Up

After the conversion is complete, you can delete the temporary PDF file, if needed.

```csharp
File.Delete(dataDir + "YourFile.cdr.pdf");
```

Congratulations! You've successfully converted a CDR file to PDF using Aspose.Imaging for .NET. This step-by-step guide should make the process straightforward for you.

## Conclusion

Aspose.Imaging for .NET is a powerful tool for handling various image formats and conversions. In this tutorial, we walked through the process of converting CDR files to PDF format, providing you with a clear and comprehensive guide to follow.

## FAQ's

### Q1: What is Aspose.Imaging for .NET?

A1: Aspose.Imaging for .NET is a .NET library for working with various image formats, enabling tasks such as conversion, manipulation, and editing.

### Q2: Do I need a license for Aspose.Imaging for .NET?

A2: Yes, you can purchase a license from [here](https://purchase.aspose.com/buy). However, you can also use a free trial from [this link](https://releases.aspose.com/) or obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/).

### Q3: Can I convert other image formats to PDF using Aspose.Imaging for .NET?

A3: Yes, Aspose.Imaging for .NET supports the conversion of various image formats to PDF.

### Q4: Is Aspose.Imaging for .NET suitable for batch conversions?

A4: Absolutely! You can use Aspose.Imaging for .NET to perform batch conversions of multiple image files to PDF.

### Q5: Where can I find additional documentation and support?

A5: You can find extensive documentation [here](https://reference.aspose.com/imaging/net/), and for support, you can visit the [Aspose forums](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
