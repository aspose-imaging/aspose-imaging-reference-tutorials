---
"description": "Aprenda a manipular metadados XMP em imagens usando o Aspose.Imaging para Java. Incorpore e recupere metadados para aprimorar seus arquivos de imagem."
"linktitle": "Tratamento de dados XMP em imagens"
"second_title": "API de processamento de imagens Java Aspose.Imaging"
"title": "Manipulação de dados XMP em imagens com Aspose.Imaging para Java"
"url": "/pt/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Manipulação de dados XMP em imagens com Aspose.Imaging para Java

Aspose.Imaging para Java é uma biblioteca versátil e poderosa para trabalhar com imagens em diversos formatos. Este tutorial guiará você pelo processo de manipulação de dados XMP (Extensible Metadata Platform) em imagens usando o Aspose.Imaging para Java. XMP é um padrão para incorporar metadados em arquivos de imagem, permitindo armazenar informações valiosas como autor, descrição e muito mais.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes pré-requisitos em vigor:

- Um ambiente de desenvolvimento Java configurado no seu computador.
- Biblioteca Aspose.Imaging para Java instalada. Você pode baixá-la do site [Site Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/).
- Um conhecimento básico de programação Java.

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

## Etapa 1: especifique o tamanho da imagem e as opções TIFF

Primeiro, defina o diretório onde sua imagem será armazenada e crie um retângulo para especificar o tamanho da imagem. Neste exemplo, usamos uma imagem Tiff com determinadas opções.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Etapa 2: Crie uma nova imagem

Agora, crie uma nova imagem com as opções especificadas. Esta imagem será usada para armazenar os metadados XMP.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Etapa 3: Criar cabeçalho e trailer XMP

Crie instâncias de XMP-Header e XMP-Trailer para seus metadados XMP. Esses cabeçalhos e trailers ajudam a definir a estrutura dos metadados.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Etapa 4: Criar Meta Informações XMP

Agora, crie uma instância do meta XMP para definir diferentes atributos. Você pode adicionar informações como autor e descrição.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Etapa 5: Criar Wrapper de Pacote XMP

Crie uma instância de XmpPacketWrapper que contenha o cabeçalho XMP, o trailer e as meta informações.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Etapa 6: Adicionar pacote do Photoshop

Para armazenar informações específicas do Photoshop, crie um pacote do Photoshop e defina seus atributos, como cidade, país e modo de cor. Em seguida, adicione esse pacote aos metadados XMP.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Etapa 7: Adicionar o pacote Dublin Core

Para informações mais gerais, como autor, título e valores adicionais, crie um pacote DublinCore e defina seus atributos. Adicione este pacote também aos metadados XMP.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Etapa 8: Atualizar metadados XMP na imagem

Atualize os metadados XMP na imagem usando o `setXmpData` método.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Etapa 9: Salve a imagem

Agora você pode salvar a imagem com os metadados XMP incorporados no disco ou em um fluxo de memória.

```java
    image.save(ms);
```

## Etapa 10: Carregue a imagem e recupere os metadados XMP

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

Parabéns! Você aprendeu com sucesso a manipular dados XMP em imagens usando o Aspose.Imaging para Java. Isso permite armazenar e recuperar metadados valiosos dentro dos seus arquivos de imagem.

## Conclusão

Neste tutorial, exploramos como trabalhar com metadados XMP em imagens usando o Aspose.Imaging para Java. Seguindo o guia passo a passo, você pode facilmente incorporar e recuperar metadados em seus arquivos de imagem, aprimorando suas informações e usabilidade.

## Perguntas frequentes

### T1: O que são metadados XMP?

R1: XMP (Extensible Metadata Platform) é um padrão para incorporar metadados em vários tipos de arquivos, incluindo imagens. Ele permite armazenar informações como autor, título, descrição e muito mais dentro do próprio arquivo.

### T2: Por que os metadados XMP são importantes?

R2: Os metadados XMP são essenciais para organizar e categorizar ativos digitais. Eles ajudam a atribuir propriedade, descrever conteúdo e adicionar contexto a arquivos como imagens, tornando-os mais acessíveis e significativos.

### P3: Posso editar metadados XMP depois de incorporá-los em uma imagem?

R3: Sim, você pode editar metadados XMP após incorporá-los a uma imagem. O Aspose.Imaging para Java fornece ferramentas para modificar e atualizar atributos de metadados conforme necessário.

### T4: O Aspose.Imaging for Java é uma ferramenta gratuita?

R4: O Aspose.Imaging para Java oferece uma versão de teste gratuita, mas para funcionalidade completa e uso prolongado, é necessária uma licença paga. Você pode explorar as opções na página [Site Aspose.Imaging para Java](https://purchase.aspose.com/buy).

### P5: Onde posso obter ajuda e suporte para o Aspose.Imaging para Java?

A5: Se você encontrar algum problema ou tiver dúvidas relacionadas ao Aspose.Imaging for Java, você pode visitar o [Fóruns Aspose.Imaging](https://forum.aspose.com/) para apoio e orientação da comunidade.



## Código-fonte completo
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
	// crie uma instância de Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// crie uma instância da metaclasse XMP para definir atributos diferentes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// crie uma instância de XmpPacketWrapper que contenha todos os metadados
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// crie uma instância do pacote Photoshop e defina os atributos do Photoshop
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// adicionar pacote do photoshop aos metadados XMP
	xmpData.addPackage(photoshopPackage);
	// crie uma instância do pacote DublinCore e defina os atributos do dublinCore
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// adicionar pacote dublinCore aos metadados XMP
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// atualizar metadados XMP na imagem
	image.setXmpData(xmpData);
	// Salvar imagem no disco ou no fluxo de memória
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

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}