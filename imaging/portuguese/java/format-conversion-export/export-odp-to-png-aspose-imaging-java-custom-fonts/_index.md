---
date: '2026-06-28'
description: Aprenda como converter ODP para PNG usando Aspose.Imaging for Java, definir
  fontes personalizadas e desativar fontes do sistema para renderização precisa.
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
title: Como converter ODP para PNG com Aspose.Imaging for Java – Guia de fontes personalizadas
  e exportação
url: /pt/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Como Converter ODP para PNG com Aspose.Imaging para Java – Fontes Personalizadas e Guia de Exportação

Em aplicações Java modernas, converter arquivos OpenDocument Presentation (ODP) em imagens PNG de alta qualidade é uma necessidade comum—especialmente quando você precisa preservar a identidade visual por meio de fontes personalizadas. Este tutorial mostra **como converter ODP** para PNG usando Aspose.Imaging para Java, orienta você a definir uma pasta de fontes personalizada, desativar fontes de fallback do sistema e ajustar finamente as opções de rasterização para desempenho ideal.

**O que você aprenderá**
- Como definir um diretório de fontes personalizado para a conversão ODP.  
- Como desativar fontes alternativas do sistema para que apenas as fontes escolhidas sejam usadas.  
- Como exportar um arquivo ODP para PNG com dimensões precisas e configurações de fonte.  
- Dicas para melhorar velocidade e uso de memória ao processar apresentações grandes.

## Respostas Rápidas
- **Posso usar Maven para adicionar Aspose.Imaging?** Sim, adicione a dependência Maven e execute `mvn install`.  
- **Preciso de uma licença para produção?** É necessária uma licença válida do Aspose.Imaging para uso ilimitado.  
- **Minhas fontes personalizadas serão respeitadas?** Defina a pasta de fontes e desative as alternativas do sistema para aplicá‑las.  
- **Quais formatos de imagem são suportados?** Aspose.Imaging suporta mais de 120 formatos raster e vetoriais, incluindo PNG, JPEG, TIFF e WebP.  
- **A API é thread‑safe?** Sim, a maioria das classes Aspose.Imaging são seguras para uso concorrente quando você cria instâncias separadas por thread.

## O que é “how to convert odp”?
*“How to convert odp”* refere‑se ao processo de transformar um arquivo OpenDocument Presentation em outro formato—geralmente PNG—preservando layout, fontes e fidelidade visual. Aspose.Imaging para Java fornece um fluxo de trabalho de método único que lida com essa conversão sem exigir ferramentas externas, permitindo que desenvolvedores integrem a conversão diretamente em suas aplicações com código mínimo.

## Por que usar Aspose.Imaging para Java?
Aspose.Imaging suporta **mais de 120 formatos de saída** e pode rasterizar arquivos ODP de várias páginas sem carregar todo o documento na memória, reduzindo o uso máximo de RAM em até 70 % em apresentações grandes. A biblioteca também oferece gerenciamento de fontes embutido, eliminando a necessidade de mecanismos de renderização de terceiros.

## Pré‑requisitos
- **Libraries**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: Version 8 or newer.  
- **IDE**: IntelliJ IDEA, Eclipse, or any Java‑compatible editor.  
- **Basic Knowledge**: Java I/O, object‑oriented programming, and image concepts.

## Instruções de Instalação

### Maven
Add the following dependency to your `pom.xml` and run `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Include the library in your `build.gradle` file and refresh the project:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Download Direto
Download the latest JAR from [Lançamentos do Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/).

## Etapas para Obtenção de Licença
To unlock full functionality, apply a temporary or permanent license:

1. **Free Trial** – No license required, limited features.  
2. **Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).  
3. **Purchase** – Buy a subscription or perpetual license from [Aspose purchase page](https://purchase.aspose.com/buy).

Initialize the library with your license file:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Como definir um diretório de fontes personalizado para conversão ODP?
`FontSettings` is a class that manages font resources for Aspose.Imaging. Load your custom fonts before any image processing begins. This ensures every slide uses the exact typefaces you provide.

Set the fonts folder path using Aspose.Imaging’s `FontSettings`:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Definition anchor*: `FontSettings.setFontsFolder` tells Aspose.Imaging where to look for TrueType and OpenType fonts on the file system.

## Como desativar fontes alternativas do sistema durante a conversão ODP?
Disabling system alternatives forces the rendering engine to ignore fonts installed on the operating system, guaranteeing that only the fonts you supply are used. This eliminates unexpected font substitutions that can alter the visual appearance of your slides.

Disable system alternatives with the following call:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Definition anchor*: `FontSettings.setGetSystemAlternativeFont(false)` forces the engine to use only the fonts located in the folder you defined, eliminating unexpected substitutions.

## Como exportar um arquivo ODP para PNG com uma fonte especificada?
`RasterizationOptions` defines how vector pages are rasterized into bitmap images. By combining font configuration with rasterization settings, you can control DPI, background color, and page size for each exported PNG.

Implement the export method as shown below:

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

*Definition anchor*: The `RasterizationOptions` class controls DPI, page size, and background color for the generated PNG files.

### Armadilhas Comuns e Soluções
- **Missing font files** – Verify that every `.ttf` or `.otf` referenced in the ODP is present in the folder you set.  
- **Incorrect file paths** – Use absolute paths or resolve relative paths against `System.getProperty("user.dir")`.  
- **Insufficient permissions** – Ensure the Java process can read the font directory and write to the output folder.

## Aplicações Práticas
1. **Brand‑consistent slide decks** – Export presentations as PNGs for web publishing while preserving corporate fonts.  
2. **Automated report generation** – Convert each slide to an image for inclusion in PDF reports or email newsletters.  
3. **Legacy archive creation** – Store ODP content as PNGs to guarantee future accessibility without needing ODP viewers.

## Considerações de Desempenho
- Use the latest Aspose.Imaging version to benefit from multi‑threaded rasterization improvements (up to 2× faster on 8‑core CPUs).  
- Wrap image processing in a try‑with‑resources block to guarantee timely disposal of native resources.  
- Adjust `RasterizationOptions` (e.g., lower DPI) when processing thousands of slides to balance quality and memory usage.

## Perguntas Frequentes

**Q: Qual é a versão mínima do Java necessária?**  
A: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended for long‑term support.

**Q: Posso converter apenas slides selecionados?**  
A: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before calling `save`.

**Q: Como lidar com arquivos ODP protegidos por senha?**  
A: Load the file with `LoadOptions` that includes the password, then proceed with the same font settings.

**Q: Desativar fontes do sistema afeta o desempenho?**  
A: It marginally improves speed because the engine skips the lookup of system fonts, especially noticeable on machines with large font collections.

**Q: Onde posso encontrar mais exemplos de código?**  
A: Explore the official [documentação do Aspose.Imaging](https://reference.aspose.com/imaging/java/) for additional scenarios such as batch conversion and image transformations.

## Recursos Adicionais
- [Lançamentos do Aspose.Imaging para Java](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Inicie seu teste gratuito](https://releases.aspose.com/imaging/java/)  
- [Documentação do Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Fórum do Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Comprar Licença Aspose](https://purchase.aspose.com/buy)  
- [Solicitar Licença Temporária](https://purchase.aspose.com/temporary-license/)  

---

**Última atualização:** 2026-06-28  
**Testado com:** Aspose.Imaging for Java 25.5  
**Autor:** Aspose

## Tutoriais Relacionados

- [Converter ODG para PNG com Aspose.Imaging para Java: Guia Completo](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Conversão Eficiente de Imagens em Java com Aspose.Imaging: Guia Completo](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}