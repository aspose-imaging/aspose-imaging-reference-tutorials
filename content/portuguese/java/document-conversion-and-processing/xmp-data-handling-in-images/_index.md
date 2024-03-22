---
title: Manipulação de dados XMP em imagens com Aspose.Imaging para Java
linktitle: Tratamento de dados XMP em imagens
second_title: API de processamento de imagem Java Aspose.Imaging
description: Aprenda como lidar com metadados XMP em imagens usando Aspose.Imaging for Java. Incorpore e recupere metadados para aprimorar seus arquivos de imagem.
type: docs
weight: 16
url: /pt/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging for Java é uma biblioteca versátil e poderosa para trabalhar com imagens em vários formatos. Este tutorial irá guiá-lo através do processo de manipulação de dados XMP (Extensible Metadata Platform) em imagens usando Aspose.Imaging for Java. XMP é um padrão para incorporar metadados em arquivos de imagem, permitindo armazenar informações valiosas como autor, descrição e muito mais.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos em vigor:

- Um ambiente de desenvolvimento Java configurado em seu computador.
-  Biblioteca Aspose.Imaging para Java instalada. Você pode baixá-lo no[Site Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/).
- Uma compreensão básica da programação Java.

## Importando Pacotes

Comece importando os pacotes necessários para o seu projeto Java. Você pode adicionar as seguintes instruções de importação no início do seu código:

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

## Etapa 1: especificar o tamanho da imagem e as opções Tiff

Primeiro, defina o diretório onde sua imagem será armazenada e crie um Retângulo para especificar o tamanho da imagem. Neste exemplo, usamos uma imagem Tiff com determinadas opções.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Etapa 2: crie uma nova imagem

Agora, crie uma nova imagem com as opções especificadas. Esta imagem será usada para armazenar os metadados XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Etapa 3: criar cabeçalho e trailer XMP

Crie instâncias de XMP-Header e XMP-Trailer para seus metadados XMP. Esses cabeçalhos e trailers ajudam a definir a estrutura de metadados.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Etapa 4: criar metainformações XMP

Agora, crie uma instância de meta XMP para definir atributos diferentes. Você pode adicionar informações como autor e descrição.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Etapa 5: criar wrapper de pacote XMP

Crie uma instância de XmpPacketWrapper que contenha o cabeçalho XMP, o trailer e as metainformações.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Etapa 6: adicionar pacote Photoshop

Para armazenar informações específicas do Photoshop, crie um pacote do Photoshop e defina seus atributos, como cidade, país e modo de cor. Em seguida, adicione este pacote aos metadados XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Etapa 7: adicionar pacote Dublin Core

Para obter informações mais gerais, como autor, título e valores adicionais, crie um pacote DublinCore e defina seus atributos. Adicione este pacote também aos metadados XMP.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Etapa 8: atualize os metadados XMP na imagem

 Atualize os metadados XMP na imagem usando o`setXmpData` método.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Etapa 9: salve a imagem

Agora você pode salvar a imagem com os metadados XMP incorporados no disco ou em um fluxo de memória.

```java
    image.save(ms);
```

## Etapa 10: carregar a imagem e recuperar metadados XMP

Para recuperar os metadados XMP da imagem, carregue a imagem do fluxo de memória ou disco e acesse os dados XMP.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Usar dados do pacote...
        }
    }
}
```

Parabéns! Você aprendeu com sucesso como lidar com dados XMP em imagens usando Aspose.Imaging for Java. Isso permite armazenar e recuperar metadados valiosos em seus arquivos de imagem.

## Conclusão

Neste tutorial, exploramos como trabalhar com metadados XMP em imagens usando Aspose.Imaging for Java. Seguindo o guia passo a passo, você pode incorporar e recuperar facilmente metadados em seus arquivos de imagem, aprimorando suas informações e usabilidade.

## Perguntas frequentes

### P1: O que são metadados XMP?

A1: XMP (Extensible Metadata Platform) é um padrão para incorporar metadados em vários tipos de arquivos, incluindo imagens. Ele permite armazenar informações como autor, título, descrição e muito mais no próprio arquivo.

### P2: Por que os metadados XMP são importantes?

A2: Os metadados XMP são essenciais para organizar e categorizar ativos digitais. Ajuda a atribuir propriedade, descrever conteúdo e adicionar contexto a arquivos como imagens, tornando-os mais acessíveis e significativos.

### P3: Posso editar metadados XMP depois de incorporá-los em uma imagem?

A3: Sim, você pode editar metadados XMP após incorporá-los em uma imagem. Aspose.Imaging for Java fornece ferramentas para modificar e atualizar atributos de metadados conforme necessário.

### Q4: O Aspose.Imaging for Java é uma ferramenta gratuita?

 A4: Aspose.Imaging for Java oferece uma versão de teste gratuita, mas para funcionalidade completa e uso estendido, é necessária uma licença paga. Você pode explorar as opções no[Site Aspose.Imaging para Java](https://purchase.aspose.com/buy).

### P5: Onde posso obter ajuda e suporte para Aspose.Imaging for Java?

 A5: Se você encontrar algum problema ou tiver dúvidas relacionadas ao Aspose.Imaging for Java, você pode visitar o[Fóruns Aspose.Imaging](https://forum.aspose.com/) para apoio e orientação da comunidade.



## Código fonte completo
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Especifique o tamanho da imagem definindo um retângulo
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// crie a nova imagem apenas para fins de amostra
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// crie uma instância do XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// crie uma instância do Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// crie uma instância da metaclasse XMP para definir atributos diferentes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//crie uma instância de XmpPacketWrapper que contenha todos os metadados
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// crie uma instância do pacote Photoshop e defina atributos do Photoshop
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// adicione o pacote photoshop aos metadados XMP
	xmpData.addPackage(photoshopPackage);
	// crie uma instância do pacote DublinCore e defina os atributos dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// adicione o pacote dublinCore aos metadados XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// atualizar metadados XMP na imagem
	image.setXmpData(xmpData);
	// Salve a imagem no disco ou no fluxo de memória
	image.save(ms);
	// Carregue a imagem do fluxo de memória ou do disco para ler/obter os metadados
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Obtendo os metadados XMP
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Usar dados do pacote...
		}
	}
}
        
```