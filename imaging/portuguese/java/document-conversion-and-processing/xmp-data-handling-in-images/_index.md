---
date: 2026-05-18
description: Aprenda a usar a biblioteca Java de processamento de imagens Aspose.Imaging
  para incorporar e recuperar metadados XMP em imagens, com código passo a passo.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: Manipulação de Dados XMP em Imagens
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
title: 'Biblioteca Java de Processamento de Imagens: XMP com Aspose.Imaging'
url: /pt/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Manipulação de Dados XMP em Imagens com Aspose.Imaging para Java

Aspose.Imaging é uma **java image processing library** que permite trabalhar com dezenas de formatos raster e vetoriais. Neste tutorial você aprenderá como incorporar e recuperar dados XMP (Extensible Metadata Platform) em imagens usando Aspose.Imaging para Java. Ao final, você poderá armazenar autor, descrição e metadados personalizados diretamente dentro dos arquivos de imagem, tornando-os pesquisáveis e auto‑descritivos.

## Respostas Rápidas
- **What is XMP?** XMP é um formato padronizado baseado em XML para incorporar metadados em arquivos como imagens, PDFs e vídeos.  
- **Which library handles XMP in Java?** Aspose.Imaging for Java fornece uma API completa para ler e escrever pacotes XMP.  
- **Do I need a license?** Um teste gratuito funciona para desenvolvimento; uma licença comercial é necessária para produção.  
- **How many image formats are supported?** Mais de 150 formatos, incluindo TIFF, JPEG, PNG, PSD e RAW.  
- **Can I process large images?** Sim – a biblioteca pode lidar com arquivos de até 2 GB sem carregar a imagem inteira na memória.

## O que são metadados XMP?
Os metadados XMP são um padrão baseado em XML que incorpora informações descritivas diretamente em arquivos digitais. Ele permite o armazenamento consistente de autor, direitos autorais, palavras‑chave e dados personalizados entre aplicativos. Como é XML, o XMP pode ser estendido com namespaces personalizados, permitindo que desenvolvedores adicionem campos proprietários enquanto permanecem compatíveis com ferramentas que entendem o esquema principal. Isso torna o XMP ideal para gerenciamento de ativos a longo prazo e interoperabilidade entre aplicações.

## Por que usar uma biblioteca Java de processamento de imagens para XMP?
Aspose.Imaging for Java suporta **150+ image formats** e pode processar arquivos multi‑gigabyte de forma streaming, reduzindo o consumo de memória em até 80 % comparado ao carregamento ingênuo. A API também garante que os pacotes XMP permaneçam em conformidade com os padrões, assegurando compatibilidade com Adobe Photoshop, Lightroom e outras ferramentas.

## Pré‑requisitos

- Um ambiente de desenvolvimento Java configurado em seu computador.  
- Biblioteca Aspose.Imaging para Java instalada. Você pode baixá‑la no [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/).  
- Um entendimento básico de programação Java.

## Importando Pacotes

Comece importando os pacotes necessários para seu projeto Java. Você pode adicionar as seguintes declarações de importação no início do seu código:

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

Agora, vamos dividir o exemplo em um guia passo a passo:

## Como incorporar metadados XMP usando uma biblioteca Java de processamento de imagens?

Carregue sua imagem, crie um pacote XMP, anexe o pacote à imagem e salve – tudo em poucas linhas concisas. O método `setXmpData` do Aspose.Imaging grava o pacote diretamente no arquivo sem exigir um arquivo de metadados separado. O processo funciona tanto com imagens baseadas em arquivo quanto em fluxo, tornando‑o adequado para serviços web e trabalhos em lote.

### Etapa 1: Especificar Tamanho da Imagem e Opções Tiff

Primeiro, defina o diretório onde sua imagem será armazenada e crie um `Rectangle` para especificar o tamanho da imagem. Neste exemplo, usamos uma imagem TIFF com certas opções. `TiffOptions` configura definições específicas de formato para a imagem TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Etapa 2: Criar uma Nova Imagem

Agora, crie uma nova imagem com as opções especificadas. Esta imagem será usada para armazenar os metadados XMP. `TiffImage` representa um objeto de imagem TIFF, e `TiffFrame` define um quadro individual dentro dela.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Etapa 3: Criar Cabeçalho e Trailer XMP

Crie instâncias de XMP‑Header e XMP‑Trailer para seus metadados XMP. Esses cabeçalhos e trailers ajudam a definir a estrutura dos metadados. `XmpHeaderPi` e `XmpTrailerPi` representam as seções de abertura e fechamento do pacote XMP.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Etapa 4: Criar Informação Meta XMP

Agora, crie uma instância de meta XMP para definir diferentes atributos. Você pode adicionar informações como autor e descrição. `XmpMeta` contém os campos principais de metadados, como autor e descrição.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Etapa 5: Criar Wrapper de Pacote XMP

`XmpPacketWrapper` é o contêiner que mantém o cabeçalho, trailer e informações meta XMP em um único pacote. Ele garante que o pacote esteja em conformidade com a especificação XMP. `XmpPacketWrapper` agrupa o cabeçalho, meta e trailer em um único pacote XMP.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Etapa 6: Adicionar Pacote Photoshop

Para armazenar informações específicas do Photoshop, crie um pacote Photoshop e defina seus atributos, como cidade, país e modo de cor. Em seguida, adicione este pacote aos metadados XMP. `PhotoshopPackage` armazena metadados específicos do Photoshop, como cidade, país e modo de cor.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Etapa 7: Adicionar Pacote Dublin Core

Para informações mais gerais, como autor, título e valores adicionais, crie um pacote DublinCore e defina seus atributos. Adicione este pacote aos metadados XMP também. `DublinCorePackage` contém campos padrão do Dublin Core, como título, criador e palavras‑chave.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Etapa 8: Atualizar Metadados XMP na Imagem

Atualize os metadados XMP na imagem usando o método `setXmpData`. Esta chamada grava o pacote XMP na seção de metadados da imagem. `setXmpData` grava o pacote XMP na seção de metadados da imagem.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Etapa 9: Salvar a Imagem

Agora você pode salvar a imagem com os metadados XMP incorporados no disco ou em um fluxo de memória.

```java
    image.save(ms);
```

### Etapa 10: Carregar a Imagem e Recuperar Metadados XMP

Para recuperar os metadados XMP da imagem, carregue a imagem a partir do fluxo de memória ou disco e acesse os dados XMP via método `getXmpData`. `getXmpData` lê o pacote XMP incorporado na imagem.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Parabéns! Você aprendeu com sucesso como manipular dados XMP em imagens usando Aspose.Imaging para Java. Isso permite armazenar e recuperar metadados valiosos dentro dos seus arquivos de imagem.

## Problemas Comuns e Soluções

- **Metadata not appearing in Photoshop:** Certifique-se de que o pacote XMP siga o esquema XML correto; Aspose.Imaging valida automaticamente, mas namespaces personalizados podem precisar de registro.  
- **Large TIFF files cause OutOfMemoryError:** Use `TiffOptions` com `Compression` definido como `LZW` e habilite streaming (`loadOptions.setBufferSize`) para manter o uso de memória baixo.  
- **Unexpected character encoding:** XMP espera UTF‑8; sempre passe strings usando `StandardCharsets.UTF_8` para evitar dados corrompidos.

## Perguntas Frequentes

**Q: O que são metadados XMP?**  
A: XMP é um padrão baseado em XML para incorporar informações descritivas diretamente em arquivos, permitindo metadados consistentes entre aplicativos.

**Q: Por que os metadados XMP são importantes?**  
A: Ele permite marcar imagens com autor, direitos autorais, palavras‑chave e dados personalizados, melhorando a capacidade de busca e o gerenciamento de ativos sem bancos de dados externos.

**Q: Posso editar os metadados XMP depois de incorporá‑los em uma imagem?**  
A: Sim, Aspose.Imaging para Java fornece métodos para modificar pacotes XMP existentes e gravá‑los de volta no arquivo.

**Q: O Aspose.Imaging para Java é uma ferramenta gratuita?**  
A: Um teste gratuito está disponível para avaliação, mas uma licença paga é necessária para uso em produção. Você pode explorar opções no [Aspose.Imaging for Java website](https://purchase.aspose.com/buy).

**Q: Onde posso obter ajuda e suporte para Aspose.Imaging para Java?**  
A: Visite os [Aspose.Imaging forums](https://forum.aspose.com/) para assistência da comunidade, ou entre em contato diretamente com o suporte da Aspose para clientes com licença paga.

## Conclusão

Neste tutorial, exploramos como trabalhar com metadados XMP em imagens usando Aspose.Imaging para Java, uma das principais **java image processing library**. Seguindo o guia passo a passo, você pode facilmente incorporar, atualizar e recuperar dados XMP, enriquecendo seus ativos digitais com metadados pesquisáveis e compatíveis com padrões.

---

**Última atualização:** 2026-05-18  
**Testado com:** Aspose.Imaging for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriais Relacionados

- [Domine o Processamento de Imagens Java: Modificar Dados EXIF com Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Processamento de Imagens Java com Aspose.Imaging: Carregando, Melhorando e Salvando Imagens](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Processamento Avançado de Imagens Java com a Biblioteca Aspose.Imaging](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


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