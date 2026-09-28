---
date: '2026-09-28'
description: Aprenda a usar ccittfax3 compression java para criar arquivos TIFF multipágina
  com Aspose.Imaging. Digitalize, arquive e reduza o tamanho dos arquivos de forma
  eficiente para fluxos de trabalho de documentos.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Descubra passo a passo como usar ccittfax3 compression java com Aspose.Imaging
  para criar arquivos TIFF multipágina eficientes para digitalização e arquivamento.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Como criar TIFF multipágina com compressão ccittfax3 java
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
title: Como criar TIFF multipágina com compressão ccittfax3 java
url: /pt/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dominando a criação de TIFF multipágina com compressão ccittfax3 java usando Aspose.Imaging

## Introdução

Se você precisa arquivar grandes volumes de documentos digitalizados mantendo os tamanhos de arquivo baixos, **ccittfax3 compression java** é a solução ideal. Este tutorial mostra como gerar arquivos TIFF multipágina com compressão CCITTFAX3 em Java usando Aspose.Imaging. Você aprenderá por que essa compressão funciona tão bem para digitalizações monocromáticas, como configurar a biblioteca e como adicionar cada página como um quadro.

**O que você aprenderá**
- Como adicionar Aspose.Imaging a um projeto Java.
- Como configurar `TiffOptions` para compressão CCITTFAX3.
- Como criar um `TiffImage`, redimensionar imagens de origem e adicioná‑las como quadros.
- Como salvar o TIFF multipágina final de forma eficiente.

Vamos percorrer a implementação completa.

## Respostas rápidas
- **Qual é o principal benefício da compressão CCITTFAX3?** Redução de até 80 % no tamanho do arquivo para digitalizações em preto‑e‑branco.  
- **Qual biblioteca fornece suporte nativo?** Aspose.Imaging para Java, versão 25.5+.  
- **Preciso de uma licença para desenvolvimento?** Uma licença de avaliação gratuita funciona para todos os recursos; uma licença paga é necessária para produção.  
- **Posso processar centenas de páginas?** Sim—Aspose.Imaging transmite as páginas, mantendo o uso de memória baixo.  
- **O código é compatível com Java 11 e posteriores?** Absolutamente; a API tem como alvo Java 8+.

## O que é ccittfax3 compression java?
`CCITTFAX3` é um algoritmo de compressão monocromático sem perdas projetado para fax e imagens de documentos digitalizados. Ele codifica cada pixel como um único bit, oferecendo saída de alta qualidade enquanto reduz drasticamente o tamanho do arquivo—geralmente de 70‑80 % em comparação com TIFF sem compressão. Isso o torna ideal para arquivar documentos em preto‑e‑branco onde a fidelidade deve ser preservada.

## Por que usar Aspose.Imaging para esta tarefa?
Aspose.Imaging suporta **mais de 100** formatos de entrada e saída, incluindo PDF, PNG, JPEG e TIFF. Sua arquitetura de streaming pode lidar com arquivos TIFF de **centenas de páginas** sem carregar todo o documento na memória, tornando‑a ideal para projetos de arquivamento em larga escala.

## Pré‑requisitos

- **Java Development Kit (JDK)** 8 ou mais recente instalado.
- **IDE** como IntelliJ IDEA ou Eclipse.
- **Maven** ou **Gradle** para gerenciamento de dependências.
- Conhecimento básico de Java (classes, objetos, coleções).

## Configurando Aspose.Imaging para Java

Adicione a biblioteca ao seu arquivo de build.

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

### Download direto

Você pode também baixar o JAR mais recente em [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Aquisição de licença

Uma licença de avaliação gratuita está disponível na [página de Avaliação Gratuita da Aspose](https://releases.aspose.com/imaging/java/). Para uso em produção, adquira uma licença permanente ou solicite uma temporária em [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Para uso detalhado da API, consulte a [documentação](https://reference.aspose.com/imaging/java/) do Aspose.Imaging para Java.

### Inicialização básica

Após adicionar a dependência, inicialize a biblioteca como mostrado abaixo.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Como configurar ccittfax3 compression java para um TIFF multipágina?

`TiffOptions` é uma classe que define o formato de saída e as configurações de compressão para um arquivo TIFF. Carregue o objeto `TiffOptions` com o enum `CCITTGroup3FaxCompression`, depois defina a origem do arquivo de saída. Essa configuração em duas etapas prepara o gravador para compressão monocromática e garante que cada página adicionada posteriormente seja codificada usando o algoritmo CCITTFAX3, resultando em redução significativa de tamanho enquanto preserva a qualidade da imagem.

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

## Como criar uma instância de TiffImage em Java?

`TiffImage` representa um documento TIFF multipágina na memória e fornece métodos para manipular seus quadros. Primeiro, defina a largura e altura que todas as páginas compartilharão. Em seguida, instancie `TiffImage` usando o `TiffOptions` criado anteriormente. O objeto `TiffImage` atua como um contêiner para os quadros individuais, permitindo adicionar, remover ou reordenar páginas antes de salvar o arquivo final.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Como carregar e redimensionar imagens de origem de uma pasta?

Filtre o diretório de destino para arquivos JPEG, leia cada imagem e redimensione‑a para corresponder ao canvas TIFF. Redimensionar antes de adicionar quadros reduz o consumo de memória e acelera a operação de salvamento. Ao converter cada imagem de origem para as dimensões e formato de pixel necessários, você garante um layout de página consistente e evita erros de tempo de execução quando os quadros são anexados ao documento TIFF.

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

## Como adicionar cada imagem como um quadro ao TIFF multipágina?

`TiffFrame` é um objeto que contém a imagem de uma única página e seus metadados associados dentro de um TIFF. Percorra as imagens redimensionadas, crie um novo `TiffFrame` e anexe‑o ao `TiffImage`. Cada quadro se torna uma página separada no documento final, e a biblioteca lida automaticamente com as atualizações necessárias de metadados, como contagem de páginas e deslocamentos, garantindo uma estrutura TIFF multipágina válida.

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

## Como salvar o arquivo TIFF multipágina final?

Chame o método `save` na instância `TiffImage`, passando o caminho de saída desejado. A biblioteca grava automaticamente todos os quadros usando compressão CCITTFAX3, transmite os dados para o disco de forma eficiente e fecha quaisquer recursos subjacentes. Após a conclusão da operação de salvamento, o arquivo resultante contém todas as páginas com a compressão especificada, pronto para distribuição ou arquivamento.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Aplicações práticas

- **Arquivamento de documentos:** Armazene contratos digitalizados, faturas ou registros legais com sobrecarga mínima de armazenamento.  
- **Imagens médicas:** Comprima exames de radiologia preservando detalhes diagnósticos.  
- **Produção de impressão:** Gere trabalhos de impressão multipágina que as impressoras podem consumir diretamente.

## Considerações de desempenho

- Use `ResizeOptions` que preservem a proporção para evitar distorção.  
- Feche cada objeto `Image` após adicionar seu quadro para liberar memória nativa.  
- Para lotes muito grandes, processe arquivos em streams paralelas e escreva cada segmento TIFF de forma assíncrona.

## Armadilhas comuns e solução de problemas

- **Formato de pixel incorreto:** CCITTFAX3 funciona apenas com imagens de 1‑bit (preto‑e‑branco). Converta imagens coloridas para escala de cinza antes de redimensionar.  
- **Vazamentos de memória:** Sempre chame `dispose()` em objetos `Image` temporários; caso contrário, os buffers nativos permanecem alocados.  
- **Tamanho do arquivo não reduzido:** Certifique‑se de que a propriedade de compressão `TiffOptions` esteja definida; caso contrário, o padrão (sem compressão) será usado.

## Perguntas frequentes

**Q: Posso usar esta abordagem com imagens coloridas?**  
A: CCITTFAX3 é limitado a dados monocromáticos; para cores use compressão JPEG ou LZW.

**Q: O Aspose.Imaging suporta streaming para TIFFs enormes?**  
A: Sim— a biblioteca grava cada quadro diretamente no stream de saída, mantendo o uso de memória baixo mesmo para milhares de páginas.

**Q: Como aplicar uma licença temporária programaticamente?**  
A: Carregue o arquivo `.lic` com `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Existe uma maneira de visualizar o TIFF antes de salvar?**  
A: Você pode renderizar cada `TiffFrame` para um `BufferedImage` e exibi‑lo em um componente Swing.

**Q: Quais versões do Java são oficialmente suportadas?**  
A: Aspose.Imaging suporta Java 8 até Java 21, incluindo versões LTS.

## Conclusão

Agora você tem um fluxo de trabalho completo e pronto para produção para criar arquivos TIFF multipágina com **ccittfax3 compression java** usando Aspose.Imaging. Seguindo os passos acima, você pode arquivar eficientemente coleções massivas de documentos mantendo os custos de armazenamento baixos e a alta qualidade de imagem. Explore recursos adicionais do Aspose.Imaging—como OCR, manipulação de metadados e conversão de formatos—para aprimorar ainda mais seu pipeline de processamento de documentos.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## Tutoriais Relacionados

- [Como criar TIFF multipágina com Aspose.Imaging para Java – Um Guia Completo](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Como reduzir o tamanho de arquivos de imagem com compressão LZW em Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Dividir quadros TIFF multipágina com Aspose.Imaging para Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}